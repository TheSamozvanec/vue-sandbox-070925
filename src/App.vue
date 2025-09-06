<script setup lang="ts">
import StartedComponent from './components/StartedComponent.vue';

</script>

<template>
  <div class="main">
  <StartedComponent/>
  </div>
</template>

<style scoped>
.main {
  margin: 1em;
  width: 98%;
  min-height: 98vh;
  background: linear-gradient(20deg, aqua 0%, aqua 5%, white 45%, white 55%, rgb(44, 255, 44) 95%, rgb(44, 255, 44));
  box-sizing: border-box;
  border: 5px ridge red;
  box-shadow: 7px 7px 5px 5px;
}
</style>
