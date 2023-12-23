<template>  
<div class="game_board">
    <div class="board_row" v-for="(row, index) in board" :key = "index">
        <div class="board_cell"
        :class="{ 'cell_empty': cell == 0, 'cell_wall': cell == 1 }"
        v-for="(cell, index) in row" :key="index">
        <!-- <div class="snake" v-for="(cell, index) in row[11]" :key = "index"> -->

        </div>
    </div>
</div>


</template>
<script setup>
import { reactive, ref } from 'vue';


const board = reactive([[1,1,1,1,1,1,1,1,1,1,1,1],
                        [1,0,0,0,0,0,0,0,0,0,0,1],
                        [1,0,0,0,0,0,0,0,0,0,0,1],
                        [1,0,0,0,0,0,0,0,0,0,0,1],
                        [1,0,0,0,0,0,0,0,0,0,0,1],
                        [1,0,0,0,0,0,0,0,0,0,0,1],
                        [1,0,0,0,0,0,0,0,0,0,0,1],
                        [1,0,0,0,0,0,0,0,0,0,0,1],
                        [1,0,0,0,0,0,0,0,0,0,0,1],
                        [1,0,0,0,0,0,0,0,0,0,0,1]])



function render_snake(direction)
{
    const dokpokdg_board = 
}


</script>
<style>
.game_board {
  display: inline-block;
  border-left: 1px solid black;
  border-top: 1px solid black;
}

.board_row {
  margin: 0;
  padding: 0;
  height: 21px;
}

.board_cell {
  display: inline-block;
  width: 20px;
  height: 20px;
  border-right: 1px solid black;
  border-bottom: 1px solid black;
}

.cell_empty {
  background-color: #f9f9f9;
}

.cell_wall {
  background-color: rgba(255, 111, 0, 0.774);
}
</style>