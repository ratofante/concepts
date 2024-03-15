<script setup>
import TextBox from '../components/Text/TextBox.vue'
import LayoutGrid from '../components/Layout/LayoutGrid.vue'
</script>
<template>
  <div>
    <div class="theme__resume">
      <LayoutGrid>
        <TextBox class="box__text">
          <template #tagNumber>01</template>
          <template #tag> theme one </template>
          <template #title>Join the game</template>
          <template #copy
            >Lorem ipsum dolor sit amet consectetur. Massa egestas sem mattis nisl ultricies egestas
            convallis tempor pellentesque. Sed nam nisi erat at tellus amet maecenas ut. Adipiscing
            ullamcorper est malesuada tempor.</template
          >
        </TextBox>
        <TextBox class="box__text" size="sm">
          <template #tagNumber>01</template>
          <template #tag> theme one </template>
          <template #title>Social Trivia</template>
          <template #copy
            >Lorem ipsum dolor sit amet consectetur. Massa egestas sem mattis nisl ultricies egestas
            convallis tempor pellentesque. Sed nam nisi erat at tellus amet maecenas ut. Adipiscing
            ullamcorper est malesuada tempor.</template
          >
        </TextBox>
      </LayoutGrid>
    </div>
  </div>
</template>

<style scoped>
.theme__resume {
  background-color: var(--clr-black);
}
.box__text {
  grid-column: 1 / -1;
}
.box__text:first-child {
  margin-bottom: 6rem;
}
</style>
