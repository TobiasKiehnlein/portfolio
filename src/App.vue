<script setup lang="ts">
import ProfilePicture from "@/components/ProfilePicture.vue";
import Overview from "@/components/Overview.vue";
import Header from "@/components/Header.vue";
</script>

<template>
  <Header/>

  <section id="home" class="grid horizontal high-contrast">
    <Overview/>
    <ProfilePicture/>
  </section>
  <section id="about" class="grid horizontal high-contrast">
    <h2>About</h2>
  </section>
  <section id="projects" class="grid horizontal high-contrast">
    <h2>Projects</h2>
  </section>
  <section id="skills" class="grid horizontal high-contrast">
    <h2>Skills</h2>
  </section>
  <section id="contact" class="grid horizontal high-contrast">
    <h2>Contact</h2>
  </section>
</template>

<style scoped lang="scss">
main {
  padding: 20px;
  overflow: visible;
}

.grid {
  display: grid;
  gap: 20px;
  grid-template-columns: auto auto;
  align-items: center;
  max-width: 100vw;
  padding: 20px;

  @media screen and (max-width: 650px) {
    grid-template-columns: auto;
    align-items: center;
    justify-content: center;

    > :last-child{
      order: -1;
    }
  }
}

</style>
