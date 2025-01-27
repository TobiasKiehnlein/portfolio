<script setup lang="ts">

</script>

<template>
  <section id="contact" class="grid horizontal high-contrast">
    <h2>Kontakt</h2>

    <div>
      <p>Ich freue mich, von Ihnen zu hören! Sie können mich über eine der folgenden Kontaktmöglichkeiten erreichen:</p>
      <div class="contact-grid">
        <span>E-Mail</span>
        <a href="mailto:tobias@kiehnlein.com">tobias@kiehnlein.com</a>
        <span>LinkedIn</span>
        <a href="https://www.linkedin.com/in/tobias-kiehnlein-97436832a" target="_blank">Mein LinkedIn Profil</a>
        <span>GitHub</span>
        <a href="https://github.com/TobiasKiehnlein" target="_blank">Mein GitHub Profil</a>
        <span>Xing</span>
        <a href="https://www.xing.com/profile/Tobias_Kiehnlein/cv" target="_blank">Mein Xing Profil</a>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
h2 {
  color: var(--color-heading);
}

p {
  color: var(--color-text);
}

.contact-grid {
  display: grid;
  gap: 20px;
  grid-template-columns: auto 1fr;
  align-items: center;
  max-width: 100vw;
  padding: 20px;

  & > span {
    font-weight: bold;

    &::after {
      content: ":";
    }
  }

  & > a {
    text-decoration: none;
    color: var(--color-primary);

    &:hover {
      text-decoration: underline;
    }
  }
}
</style>