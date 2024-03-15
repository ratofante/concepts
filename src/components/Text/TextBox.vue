<template>
  <div class="box__text">
    <div class="tag" :class="`tag-${size}`">
      <span class="number" :class="`number-${size}`">
        <slot name="tagNumber"></slot>
      </span>
      <slot name="tag"></slot>
    </div>
    <div class="title" :class="`title-${size}`">
      <slot name="title"></slot>
    </div>
    <div class="copy" :class="`copy-${size}`">
      <slot name="copy"></slot>
    </div>
  </div>
</template>

<script setup>
defineProps({
  size: {
    type: String,
    default: 'md',
    validator(value) {
      return ['sm', 'md'].includes(value)
    }
  }
})
</script>

<style scoped>
.tag {
  font-family: 'Jura', Arial, Helvetica, sans-serif;
  font-size: 1.15rem;
  color: var(--clr-dark-gray);
  text-transform: uppercase;
  font-weight: 600;
  letter-spacing: 2px;
  padding-bottom: 1rem;
}
.number {
  color: var(--clr-fucsia);
}
.number-sm,
.tag-sm {
  font-size: 1rem;
}
.title {
  font-family: 'Jura', Arial, Helvetica, sans-serif;
  font-size: 4rem;
  font-weight: 500;
  color: var(--clr-light-pink);
  margin-bottom: 1.8rem;
}
.title-sm {
  font-size: 2.8rem;
  text-transform: uppercase;
  margin-bottom: 1rem;
}
.copy {
  color: var(--clr-light-gray);
  opacity: 85%;
  font-size: 1.2rem;
  font-weight: 300;
  line-height: 1.8;
}
.copy-sm {
  font-size: 1rem;
}
</style>
