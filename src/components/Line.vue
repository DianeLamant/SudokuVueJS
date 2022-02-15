<script setup>
import Box from './Box.vue'

defineProps({
    line: Array
})
</script>

<template>
  <div class="line">
    <Box v-for="box in line" v-bind:box="box"></Box>
  </div>
</template>

<style scoped>
.line {
    display: flex;
    width: min-content;
}
.line:first-of-type {
    border-top: 2px solid white;
}
.line:nth-child(3n) {
    border-bottom: 2px solid white;
}
</style>
