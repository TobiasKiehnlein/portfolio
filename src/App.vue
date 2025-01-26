<script setup lang="ts">
import Home from "@/components/Home.vue";
import Header from "@/components/Header.vue";
import About from "@/components/About.vue";
import Skills from "@/components/Skills.vue";
</script>

<template>
  <Header/>

  <Home/>

  <About/>
  <section id="projects" class="grid horizontal high-contrast">
    <h2>Projects</h2>
  </section>
    <Skills/>
  <section id="contact" class="grid horizontal high-contrast">
    <h2>Contact</h2>
  </section>
</template>

<style scoped lang="scss">
main {
  padding: 20px;
  overflow: visible;
}

//.grid {
//  display: grid;
//  gap: 20px;
//  grid-template-columns: auto auto;
//  align-items: center;
//  max-width: 100vw;
//
//  @media screen and (max-width: 650px) {
//    grid-template-columns: auto;
//    align-items: center;
//    justify-content: center;
//
//    &.inverted > :last-child {
//      order: -1;
//    }
//  }
//}

</style>
