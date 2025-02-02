<script setup lang="ts">

</script>

<template>
  <div class="profilePic">
    <img src="../assets/profile_transparent.png" alt="Profile Picture"/>
    <div class="blob"></div>
    <div class="blob"></div>
    <div class="blob"></div>
    <div class="blob"></div>
    <div class="blob"></div>
  </div>
</template>

<style scoped lang="scss">

.profilePic {
  filter: url('#goo') drop-shadow(0 .5rem .5rem var(--color-glow));
  aspect-ratio: 1;
  width: 40vw;
  height: 45vw;
  max-width: 400px;
  max-height: 450px;
  position: relative;
  overflow: visible;
  z-index: -1;
  margin: auto;

  &::before {
    content: '';
    clip-path: polygon(50% 0, 100% 25%, 100% 75%, 50% 100%, 0 75%, 0 25%);
    background: var(--color-primary);
    position: absolute;
    inset: 0;
    z-index: -2;
  }

  .blob {
    position: absolute;
    z-index: -1;
    width: 30%;
    height: 30%;
    inset: 0;
    margin: auto;

    &::after {
      content: '';
      clip-path: polygon(50% 0, 100% 25%, 100% 75%, 50% 100%, 0 75%, 0 25%);
      background: var(--color-primary);
      position: absolute;
      inset: 0;
      margin: auto;
      width: var(--width, 0);
      height: var(--width, 0);
    }

    $duration: 60s;
    $delay: -30s;
    animation: randomMovement $duration alternate infinite;

    &:nth-child(2) {
      animation-delay: $delay;

      --width: 30%;
    }

    &:nth-child(3) {
      animation-delay: $duration * 0.3 + $delay;
      --width: 80%;
    }

    &:nth-child(4) {
      animation-delay: $duration * 0.6 + $delay;
      --width: 50%;
    }

    &:nth-child(5) {
      animation-delay: $duration * 0.9 + $delay;
      --width: 70%;
    }

    &:nth-child(6) {
      animation-delay: $duration * 1.2 + $delay;
      --width: 40%;
    }
  }

  img  {
    width: 110%;
    height: 110%;
    object-fit: contain;
    clip-path: polygon(0 0, 100% 0, 100% 75%, 50% 100%, 0 75%, 0 25%);
    //transform: scaleX(-1);
    position: absolute;
    bottom: 0;
    left: -50%;
    right: -50%;
    margin: auto;
  }
}

@keyframes randomMovement {
  $factor: 3;

  0% {
    transform: translate(0, 0);
  }

  20% {
    transform: translate(-87.7% * $factor, 40.5% * $factor);
  }

  40% {
    transform: translate(75.4% * $factor, -33.0% * $factor);
  }

  60% {
    transform: translate(-34.1% * $factor, 67.4% * $factor);
  }

  80% {
    transform: translate(64.2% * $factor, 49.1% * $factor);
  }

  100% {
    transform: translate(-90.0% * $factor, -40.0% * $factor);
  }
}
</style>