<script setup>
import Cell from './Cell.vue'
const props = defineProps({ blockIndex : Number })
</script>
<template>
  <div class="block">
    <Cell v-for="i in 9" :key="i" :blockIndex="props.blockIndex" :index="i - 1" /> 
  </div>
</template>
<style scoped>
.block {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  grid-template-rows: repeat(3, 1fr);
  border: 3px solid black;
  width: fit-content;
  height: fit-content;
}
</style>
