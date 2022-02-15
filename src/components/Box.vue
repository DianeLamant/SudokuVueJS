<script setup>

defineProps({
    box: Number
})

</script>

<template>
  <div class="box">
    <p v-if="box > 0">{{ box }}</p>
  </div>
</template>

<style scoped>
.box {
  width: 58px;
  height: 58px;
  border: 1px solid #ffffff7a;
  display: flex;
  align-items: center;
  justify-content: center;
}
.box:first-of-type {
  border-left: 3px solid white;
}
.box:nth-child(3n) {
  border-right: 3px solid white;
}
p {
  color: white;
  font-size: 24px;
  font-weight: bold;
}
</style>
