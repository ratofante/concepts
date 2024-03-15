<script>
import { onMounted, ref } from 'vue'
const bubbles = ref()

onMounted(() => {
  console.log(bubbles.value)
})
</script>
<template>
  <div class="container">
    <div v-for="n in 4" :key="n" class="bubble" ref="bubbles"></div>
  </div>
</template>

<style scoped></style>
