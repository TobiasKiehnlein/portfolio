<script setup lang="ts">

</script>

<template>
  <section id="contact" class="grid horizontal high-contrast">
    <h2>Kontakt</h2>

    <div>
      <p>Ich freue mich, von Dir zu hören! Du erreichst mich über folgende Kontaktmöglichkeiten:</p>
      <div class="contact-grid">
        <span><i style='background-image: url("/brand-logos/envelope.svg")'/></span>
        <a href="mailto:tobias@kiehnlein.com">tobias@kiehnlein.com</a>
        <span><i style='background-image: url("/brand-logos/github.svg")'/></span>
        <a href="https://github.com/TobiasKiehnlein" target="_blank">Mein GitHub Profil</a>
        <span><i style='background-image: url("/brand-logos/linkedin.svg")'/></span>
        <a href="https://www.linkedin.com/in/tobias-kiehnlein-97436832a" target="_blank">Mein LinkedIn Profil</a>
        <span><i style='background-image: url("/brand-logos/xing.svg")'/></span>
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

  i {
    width: 25px;
    height: 25px;
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
display: inline-flex;
  }

  & > span {
    font-weight: bold;
    display: inline-flex;
    align-items: end;

    //&::after {
    //  content: ":";
    //}
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