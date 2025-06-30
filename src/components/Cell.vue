<script setup>
import { inject } from 'vue'
const props = defineProps({
  blockIndex: Number,
  index: Number
})
const board = inject('board')

let row = Math.floor(props.blockIndex / 3) * 3 + Math.floor(props.index / 3)  
let column = (props.blockIndex % 3) * 3 + props.index % 3
const cellNumber = board[row][column]
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
