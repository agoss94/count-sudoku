<script setup>
import { inject } from 'vue'
const props = defineProps({
  row: Number,
  column: Number,
})
const board = inject('board')
const cellNumber = board[props.row][props.column]
</script>
<template>
  <div class="cell">
    {{cellNumber === 0 ? '' : cellNumber}} 
  </div>
</template>
<style scoped>
.cell {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 50px;
  height: 50px;
  border: 1px solid #ccc;
  box-sizing: border-box;
  font-size: 30px;
  font-weight: bold;
}
</style>
