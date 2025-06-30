
<script setup>
  import Block from './Block.vue'  
</script>
<template>
  <div class="board">
    <Block v-for="i in 9" :key="i" :blockIndex="i - 1" /> 
  </div>
</template>
<style scoped>
.board { 
  display: grid;
  grid-template-columns: repeat(3, auto);
  grid-template-row: repeat(3, auto);
  gap: 0;
  width: fit-content;
  height: fit-content;
  border: 3px solid black;
} 
</style>
