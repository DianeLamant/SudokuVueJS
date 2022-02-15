<script setup>

import Line from './Line.vue'
import Grids from '../assets/large1.json'

const QUIZZES = "quizzes";
const SOLUTIONS = "solutions";
const MAX_NUMBER = 9;

const gridNumber = Math.floor(Math.random() * Grids.length);
const grid = Grids[gridNumber];
const startingGrid = grid[QUIZZES];

let colStart = 0;
let colNumber = MAX_NUMBER;
let rowNumber = MAX_NUMBER;

// Create an array containing an array of number for each line of the grid
let lines = [];
for(let r=0; r<rowNumber; r++) {
  let line = [];
  for(let i=colStart; i<colNumber; i++) {
    let number = parseInt(startingGrid[i]);
    line.push(number);
  }
  colStart += MAX_NUMBER;
  colNumber += MAX_NUMBER;
  lines.unshift(line);
}

</script>

<template>
  <div class='grid'>
    <Line v-for="line in lines" v-bind:line="line"></Line>
  </div>
</template>

<style scoped>

.grid {
  width: fit-content;
  border: 1px solid white;
}

</style>