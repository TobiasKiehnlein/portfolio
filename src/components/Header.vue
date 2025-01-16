<script setup lang="ts">
import {ref} from "vue";
import NavLinks from "@/components/NavLinks.vue";

const menuOpen = ref(false);
</script>

<template>
  <div :class="'backdrop ' + (menuOpen?'open':'closed')" @click="menuOpen=false"></div>
  <header :class="menuOpen?'open':'closed'">
    <span>Tobias <span primary>Kiehnlein</span></span>
    <i :class="menuOpen?'open':'closed'" @click="menuOpen=!menuOpen"></i>
    <nav :class="menuOpen?'open':'closed'">
      <NavLinks v-model:menu-open="menuOpen"/>
    </nav>
  </header>
</template>

<style scoped lang="scss">
header {
  font-weight: bold;
  position: fixed;
  display: flex;
  top: 0;
  left: 0;
  right: 0;
  height: 40px;
  padding: 40px 20px;
  background-color: var(--color-background);
  z-index: 10;
  align-items: center;

  transition: all .5s;

  &.open {
    background-color: transparent;

    > span {
      opacity: 0;
    }
  }

  > i {
    z-index: 10;
    width: 20px;
    height: 3px;
    background: var(--color-text);
    border-radius: 9999999px;
    position: relative;
    transition: all .5s;

    &.open {
      background: transparent;

      &::before {
        top: 0;
        transform: rotate(45deg);
      }

      &::after {
        top: 0;
        transform: rotate(-45deg);
      }
    }

    &::before, &::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 3px;
      background: var(--color-text);
      border-radius: 9999999px;
      transition: all .5s;
    }

    &::before {
      top: -8px;
    }

    &::after {
      top: 8px;
    }
  }

  > span {
    flex: 1;
    font-size: 1.5rem;
    transition: all .5s;
  }

  nav {
    display: flex;
    justify-content: space-around;
    align-items: center;
    gap: 20px;

    @media screen and (max-width: 650px) {
      position: fixed;
      right: -100%;
      top: 0;
      justify-content: center;
      flex-direction: column;
      transition: right .5s;
      min-width: 200px;
      max-width: 400px;
      width: 40vw;
      height: 100vh;
      z-index: 9;
      background-color: var(--color-background);
      filter: drop-shadow(0 0 10px var(--color-border-hover));

      &.open {
        right: 0;

      }
    }
  }

}

.backdrop {
  pointer-events: none;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: 100vh;
  transition-property: all;
  transition-duration: .5s;
  z-index: 9;
  backdrop-filter: none;

  &.open {
    pointer-events: all;
    backdrop-filter: blur(10px);
  }
}
</style>