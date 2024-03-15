<script setup>
import LoaderBubbles from '@/components/LoaderBubbles.vue'
import { onMounted, ref } from 'vue'

const texts = ref()

onMounted(() => {
  console.log(texts.value)
})
</script>
<template>
  <div class="loader">
    <div class="loader__container">
      <div class="loader__header">
        <h6 class="loader__title">
          <span class="loader__title__word">Concept</span>
          <span class="loader__title__number">One</span>
        </h6>
      </div>
      <div class="loader__image">
        <img src="@/assets/img/loading.jpg" alt="" srcset="" />
      </div>
      <div class="loader__display">
        <p>
          <span
            v-for="(text, i) in [
              'Loading aesthetics',
              'Spawning creativity',
              'Keeping control',
              'Breathe'
            ]"
            ref="texts"
            class="loader__text"
            :key="i"
            >{{ text }}</span
          >
        </p>
        <LoaderBubbles />
      </div>
    </div>
  </div>
</template>

<style scoped>
.loader {
  display: grid;
  place-items: center;
  min-height: 100svh;
  background-color: #171717;
}
.loader__title {
  margin-bottom: max(4vh, 20px);
  font-family: 'Jura', 'Inter', Arial, serif;
  color: #d9d9d9;
  text-align: center;
  letter-spacing: -1px;
  line-height: 1;
}
.loader__title > span {
  display: block;
}
.loader__title__word {
  font-size: 32px;
  color: #925492;
}
.loader__title__number {
  font-size: 18px;
  color: #d9d9d9;
}
.loader__image {
  margin: auto;
  width: 175px;
}
.loader__image img {
  width: 100%;
}
.loader__display {
  margin-top: min(4vh, 20px);
}
.loader__display p {
  position: relative;
  text-align: center;
  width: fit-content;
  margin: auto;
  overflow-y: hidden;
}
.loader__text {
  display: block;
  font-family: 'Inter', Helvetica, system-ui, sans-serif;
  color: #7d587d;
  font-size: 12px;
}
.loader__text:not(:first-child) {
  position: absolute;
}
</style>
