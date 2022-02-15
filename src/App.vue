<script setup>
import Sudoku from './components/Sudoku.vue'
</script>

<template>
  <header></header>

  <main>
    <h1>Sudoku</h1>
    <Sudoku />
  </main>
</template>

<style>
@import './assets/base.css';

body {
  background: linear-gradient(70deg, #64e2ff, #9544ff);
}

main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 80%;
  height: 80%;
  margin: auto;
}

h1 {
  font-size: 70px;
  color: white;
  text-shadow: 1px 1px 6px black;
  font-weight: bold;
  line-height: 2em;
}
</style>
