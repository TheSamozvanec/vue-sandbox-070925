<template>
    <div>
        <h1 class="head-text">Стартовая страница</h1>
        <OptionsOne/>
        <OptionsTwo/>
        <CompositionOne/>
        <CompositionTwo/>
    </div>
</template>

<script setup lang="ts">
import CompositionOne from './CompositionOne.vue';
import CompositionTwo from './CompositionTwo.vue';
import OptionsOne from './OptionsOne.vue';
import OptionsTwo from './OptionsTwo.vue';


</script>

<style scoped>
    .head-text{
        text-align: center;
    }
    .content {
        margin: 1em auto;
        padding: 10px;
        width: 90%;
        min-height: 15vh;
        background: rgba(233, 37, 37, 0.5);
        border: 1px solid black;
    }
</style>