<script setup lang="ts">
import ProfilePicture from "@/components/ProfilePicture.vue";
import Overview from "@/components/Overview.vue";
import Header from "@/components/Header.vue";
</script>

<template>
  <Header/>

  <section id="home" class="grid horizontal high-contrast inverted">
    <Overview/>
    <ProfilePicture/>
  </section>
  <section id="about" class="grid horizontal high-contrast">
    <h2>About</h2>
    <div>
      <p>
        Ich bin ein leidenschaftlicher Web-Fullstack-Entwickler mit fundiertem Wissen in der Softwareentwicklung.
        Bereits seit meiner Schulzeit arbeite ich daran, technische Probleme mit innovativen Lösungen zu bewältigen.
        Neben meinen beruflichen praktischen Erfahrungen habe ich während meines Informatikstudiums auch tiefgehende theoretische Kenntnisse erlangt.
      </p>
    </div>
  </section>
  <section id="projects" class="grid horizontal high-contrast">
    <h2>Projects</h2>
  </section>
  <section id="skills" class="grid horizontal high-contrast">
    <h2>Skills</h2>

    <div>
      <h3>Frontend</h3>
      <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
        <li>Vue.js</li>
        <li>React</li>
        <li>Angular</li>
      </ul>

      <h3>Backend</h3>
      <ul>
        <li>Node.js</li>
        <li>Express</li>
        <li>dotNET</li>
        <li>Python</li>
        <li>Java</li>
      </ul>

      <h3>Database</h3>
      <ul>
        <li>MySQL</li>
        <li>PostgreSQL</li>
        <li>SQLite</li>
        <li>Redis</li>
        <li>MSSQL</li>
      </ul>

      <h3>DevOps</h3>
      <ul>
        <li>Docker (Swarm)</li>
        <li>Gitlab</li>
        <li>GitHub Actions</li>
        <li>Ansible</li>
        <li>fastlane</li>
      </ul>
    </div>
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

    &.inverted > :last-child {
      order: -1;
    }
  }
}

</style>
