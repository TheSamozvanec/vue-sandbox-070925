<template>
    <div class="content options-one">
        <p class="title">Options API first component</p>
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

<script lang="ts">
import { colors } from '@/data/data';
import { defineComponent } from 'vue'

export default defineComponent({
    data () {
        return{
            inputText:'',
            color:colors[0],
            toggle:0
        }
    },
    methods: {
        insertColor(){
            this.toggle = this.toggle>=(colors.length-1)? 0 : this.toggle+=1;
            this.color = colors[this.toggle] 
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