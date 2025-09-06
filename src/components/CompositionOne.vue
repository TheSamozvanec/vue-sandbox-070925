<template>
    <div class="content options-one">
        <p class="title">Composition API first component</p>
        <p class="view-text">{{'Ввод: '+inputText}}</p>
        <input 
        class="input"
        v-model="inputText" 
        type="text" />
        <button 
        @click="insertColor"
        :class="color">{{color}}</button>
        <div class="black"></div>
        <p class="empty">{{  }}</p>
    </div>
</template>

<script setup lang="ts">
import { colors } from '@/data/data';
import { ref } from 'vue';
    const inputText = ref<string>('');
    const color = ref<string>(colors[0]);
    const toggle =ref<number>(0)
    function insertColor(){
        toggle.value = toggle.value>=(colors.length-1)? 0 : toggle.value+=1;
        color.value = colors[toggle.value] 
    }

</script>

<style scoped>
    .options-one {
        display: grid;
        grid-template: repeat(2, 1fr) / repeat(5, 1fr);
    } 
    .title {
        grid-column: 1 / 6;
    }
    .input {
        height: 3vh;
    }
    .view-text, .empty{
        overflow: hidden;
    }
    .blue {
        background: blue;
    }
    .green {
        background: green;
    }
    .yellow {
        background: yellow;
    }
    .red {
        background: red;
    }
    .black {
        background: black;
    }

</style>