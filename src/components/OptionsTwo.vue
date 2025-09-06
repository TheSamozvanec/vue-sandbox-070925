<template>
    <div class="content options-one">
        <p class="title">Options API second component</p>
        <p class="view-text">{{'Ввод: '+inputText}}</p>
        <input 
        class="input"
        v-model="inputText" 
        type="text" />
        <p class="empty">{{  }}</p>
        <div class="black"></div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    data () {
        return{
            inputText:'',
        }
    },
    
})
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