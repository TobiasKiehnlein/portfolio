<script setup lang="ts">

import ProfilePicture from "@/components/ProfilePicture.vue";
</script>

<template>
  <section id="home" class="grid horizontal high-contrast inverted">
    <div>
      <span class="top-line">Hello, <span primary>I'm</span></span>
      <h1 primary>Tobias Kiehnlein</h1>
      <h2>Full-stack Developer</h2>
      <p>Passion for modern web development and automation.</p>
      <a href="#contact">
        <button>Let's talk</button>
      </a>
    </div>
    <ProfilePicture/>
  </section>

</template>

<style scoped lang="scss">
.grid {
  display: grid;
  gap: 20px;
  grid-template-columns: auto auto;
  align-items: center;
  max-width: 100vw;

  @media screen and (max-width: 650px) {
    grid-template-columns: auto;
    align-items: center;
    justify-content: center;

    &.inverted > :last-child {
      order: -1;
    }
  }
}

h1 {
  font-size: 3em;
  font-weight: bold;
  filter: drop-shadow(0px 0px 3px var(--color-background));
  z-index: 1;
}

div {
  display: flex;
  flex-direction: column;
  justify-content: center;

  .top-line {
    font-size: 1.5em;
    font-weight: bold;
  }

  button {
    align-self: flex-start;
    padding: 15px 30px;
    margin-top: 40px;
  }
}

div, h2 {
  font-weight: bold;
}

p {
  margin-top: 20px;
  opacity: .5;
}

</style>