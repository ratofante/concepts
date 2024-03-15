<template>
  <div class="grid">
    <slot />
  </div>
</template>

<script setup></script>

<style scoped>
.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  padding-block: 3rem;
  margin-inline: 1.5rem;
}
</style>
