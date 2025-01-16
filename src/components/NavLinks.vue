<script setup lang="ts">
const menuOpen = defineModel<boolean>('menuOpen', {required: true});
</script>

<template>
  <a href="#home" @click="menuOpen=false">Home</a>
  <a href="#about" @click="menuOpen=false">About</a>
  <a href="#projects" @click="menuOpen=false">Projects</a>
  <a href="#skills" @click="menuOpen=false">Skills</a>
  <a href="#contact" @click="menuOpen=false">Contact</a>
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