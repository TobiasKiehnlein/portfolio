<script setup lang="ts">
const menuOpen = defineModel<boolean>('menuOpen', {required: true});
</script>

<template>
  <a href="#home" @click="menuOpen=false">Start</a>
  <a href="#about" @click="menuOpen=false">Über mich</a>
  <a href="#projects" @click="menuOpen=false">Projekte</a>
  <a href="#skills" @click="menuOpen=false">Skills</a>
  <a href="#contact" @click="menuOpen=false">Kontakt</a>
</template>

<style scoped lang="scss">
a {
  text-decoration: none;
  color: var(--text-color);

  &:hover {
    color: var(--color-primary);
    cursor: pointer;
  }
}
</style>