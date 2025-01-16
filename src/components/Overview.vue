<script setup lang="ts">

</script>

<template>
  <div>
    <span class="top-line">Hello, <span primary>I'm</span></span>
    <h1 primary>Tobias Kiehnlein</h1>
    <h2>Full-stack Developer</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
    <a href="#contact"><button>Let's talk</button></a>
  </div>
</template>

<style scoped lang="scss">
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