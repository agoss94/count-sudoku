<script setup>
import Cell from './Cell.vue'
const props = defineProps({ blockIndex : Number })

function calculateRow(blockIndex, index) {
  return Math.floor(blockIndex / 3) * 3 + Math.floor(index / 3)  
}

function calculateColumn(blockIndex, index) {
  return (blockIndex % 3) * 3 + index % 3
}

</script>
<template>
  <div class="block">
    <Cell v-for="i in 9" 
      :key="i" 
      :row="calculateRow(props.blockIndex, i - 1)"
      :column="calculateColumn(props.blockIndex, i - 1)"
    /> 
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
