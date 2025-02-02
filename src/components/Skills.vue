<script setup lang="ts">
const entries = {
  Frontend: [
    {name: 'HTML', icon: 'html.svg', skill: 4.5},
    {name: 'CSS', icon: 'css-3.svg', skill: 5},
    {name: 'SASS', icon: 'sass.svg', skill: 5},
    {name: 'JavaScript', icon: 'javascript.svg', skill: 5},
    {name: 'TypeScript', icon: 'typescript.svg', skill: 4.5},
    {name: 'Vue.js', icon: 'vue.svg', skill: 4.5},
    {name: 'React', icon: 'react.svg', skill: 4.5},
    {name: 'Angular', icon: 'angular.svg', skill: 4.5},
    {name: 'Ionic', icon: 'ionic.svg', skill: 4.5},
  ],
  Backend: [
    {name: 'Node.js', icon: 'nodejs.svg', skill: 4.5},
    {name: 'dotNET', icon: 'dotnet.svg', skill: 4},
    {name: 'Python', icon: 'python.svg', skill: 4},
    {name: 'Java', icon: 'java.svg', skill: 3.5},
  ],
  Database: [
    {name: 'MySQL', icon: 'mysql.svg', skill: 4},
    {name: 'PostgreSQL', icon: 'postgresql.svg', skill: 4},
    {name: 'SQLite', icon: 'sqlite.svg', skill: 4},
    {name: 'Redis', icon: 'redis.svg', skill: 4},
    {name: 'MSSQL', icon: 'mssql.svg', skill: 4},
  ],
  DevOps: [
    {name: 'Docker (Swarm)', icon: 'docker.svg', skill: 5},
    {name: 'Gitlab', icon: 'gitlab.svg', skill: 5},
    {name: 'GitHub Actions', icon: 'github.svg', skill: 5},
    {name: 'Ansible', icon: 'ansible.svg', skill: 4},
    {name: 'fastlane', icon: 'fastlane.svg', skill: 4.5},
  ],
  'Operating Systems': [
    {name: 'Linux', icon: 'linux-tux.svg', skill: 5},
    {name: 'macOS', icon: 'mac-os.svg', skill: 5},
    {name: 'Windows', icon: 'windows.svg', skill: 4.5},
    {name: 'Android', icon: 'android.svg', skill: 5},
    {name: 'iOS', icon: 'iOS.svg', skill: 4.5},
  ],
}
</script>

<template>

  <section id="skills" class="grid horizontal high-contrast">
    <h2>Skills</h2>

    <div v-for="(entries, category) in entries" :key="category">
      <h3>{{ category }}</h3>
      <ul>
        <li v-for="entry in entries" :key="entry.name">
          <img :src="`/brand-logos/${entry.icon}`" :alt="entry.name">
          <span>{{ entry.name }}</span>
        </li>
      </ul>
    </div>
  </section>

</template>

<style scoped lang="scss">

.grid {
  display: grid;
  gap: 20px;

  h3 {
    margin-top: 20px;
    color: var(--color-heading);
  }

  ul {
    display: grid;
    gap: 20px;
    grid-template-columns: repeat(auto-fill, minmax(min(100px, 20vw), 1fr));
    align-items: center;
  }

  li {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    flex-direction: column;
    position: relative;
    aspect-ratio: 0.8660254326;
    filter: url('#goo') drop-shadow(0 .5rem .5rem var(--color-background-mute));
    padding: 10px;
    animation: subtle-random-movement 30s infinite ease-in-out;

    // for loop for animation offset
    @for $i from 1 through 80 {
      &:nth-child(#{$i}) {
        animation-delay: -#{$i * $i * $i * $i % 29}s;
      }
    }

    &:hover {
      filter: saturate(1) url('#goo') drop-shadow(0 .5rem .5rem var(--color-glow));
      color: white;

      &::before {
        background: var(--color-primary);
      }
    }

    &::before {
      content: '';
      position: absolute;
      inset: 0;
      z-index: -1;
      clip-path: polygon(50% 0, 100% 25%, 100% 75%, 50% 100%, 0 75%, 0 25%);
      background-color: var(--color-background-soft);
      transition: background-color .3s;
    }

    span {
      text-align: center;
    }
  }

  img {
    width: 30px;
    height: 30px;
    filter: drop-shadow(0 0 10px var(--color-background));
  }
}

@keyframes subtle-random-movement {
  0% {
    transform: translate(0, 0);
  }
  10% {
    transform: translate(-3px, 2px);
  }
  20% {
    transform: translate(2px, -1px);
  }
  30% {
    transform: translate(-2px, -3px);
  }
  40% {
    transform: translate(4px, 1px);
  }
  50% {
    transform: translate(-1px, 3px);
  }
  60% {
    transform: translate(3px, -2px);
  }
  70% {
    transform: translate(-4px, 2px);
  }
  80% {
    transform: translate(1px, -3px);
  }
  90% {
    transform: translate(-2px, 1px);
  }
  100% {
    transform: translate(0, 0);
  }

}
</style>