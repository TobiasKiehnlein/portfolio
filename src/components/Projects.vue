<script setup lang="ts">
interface Project {
  title: string;
  technologies?: string;
  description: string;
}

const introText: string = `
Im Laufe meiner bisherigen Tätigkeit in der Softwareentwicklung
konnte ich an unterschiedlichen Projekten mitwirken. Dabei habe
ich nicht nur vielfältige Technologien und Frameworks kennengelernt,
sondern auch meine Fähigkeiten in Architektur, DevOps und Testing
stetig vertieft. Einige ausgewählte Projekte stelle ich hier vor:
`;

const projects: Project[] = [
  {
    title: "1. AnnApp",
    technologies: "React Native, Expo, WebDav",
    description:
        "Diese App entstand im Rahmen meines P-Seminars und wurde " +
        "anschließend sowohl im Google Play Store als auch im " +
        "Apple App Store veröffentlicht. Sie bietet Zugriff auf " +
        "Vertretungspläne, Hausaufgaben und weitere schulrelevante " +
        "Informationen. Durch die Zusammenarbeit mit Fujitsu " +
        "wurde das Projekt unter anderem mit dem SCHULEWIRTSCHAFTPREIS " +
        "2018 ausgezeichnet. Dabei konnte ich erste Erfahrungen " +
        "im Bereich der Projektleitung sammeln – auch wenn es sich " +
        "um ein schulisches Umfeld handelte, hat mir dies sehr " +
        "geholfen, erste Schritte im Teammanagement zu machen."
  },
  {
    title: "2. SIRADOS (CubeFour)",
    technologies: "AngularJS, LESS, .NET Framework 4.5",
    description:
        "Als Einstieg in die Webentwicklung habe ich bei CubeFour " +
        "an SIRADOS mitgewirkt, einer führenden Software im Bereich " +
        "Baukostenplanung und Ausschreibung. Hier konnte ich meine " +
        "Fullstack-Kompetenzen ausbauen und wertvolle Erfahrungen " +
        "im Umgang mit großen Codebasen sammeln."
  },
  {
    title: "3. AWIDO",
    technologies: "Ansible, Gitlab CI, fastlane, Docker Swarm, .NET 4.7, Angular, MSSQL",
    description:
        "Im Rahmen der Weiterentwicklung von AWIDO, einer Plattform " +
        "im Bereich Abfallwirtschaft, war ich für neue Features und " +
        "die Implementierung automatisierter Deployment-Prozesse " +
        "verantwortlich. Dadurch konnten über 50 Apps, die " +
        "eine gemeinsame Codebasis haben, automatisiert " +
        "im PlayStore und AppStore veröffentlicht werden."
  },
  {
    title: "4. Angular-Upgrades",
    technologies: "Angular (Version 6 bis 18), TypeScript",
    description:
        "In mehreren Projekten habe ich Angular-Anwendungen " +
        "modernisiert. Dabei ging es um das schrittweise Upgrade " +
        "von Version 6 auf Version 18, inklusive Refactoring und " +
        "Performance-Optimierung. Diese Arbeiten erforderten ein " +
        "tiefes Verständnis der Angular-Architektur sowie den " +
        "Umgang mit Breaking Changes."
  },
  {
    title: "5. Adblocker/Trackingblocker",
    technologies: "Lokale KI, JavaScript",
    description:
        "In diesem Projekt entwickelte ich einen Adblocker, der " +
        "Nutzer- und Trackingdaten lokal verarbeitet, ohne Daten " +
        "an externe Server zu senden. Obwohl das Projekt nie " +
        "veröffentlicht wurde, konnte ich sehr viel über die " +
        "Funktionsweise von Browsern lernen: Wie Websites tracken, " +
        "auf welche verschiedenen Arten und Weisen Requests ausgelöst werden können und vieles " +
        "mehr, was man im normalen Entwickleralltag kaum bedenken muss."
  },
  {
    title: "6. XITASO Universitätsprojekt",
    technologies: "Blazor Server, Azure Pipelines, GitLab, E2E Tests mit Playwright",
    description:
        "Gemeinsam mit meinem Team habe ich im Rahmen des Softwareprojektes an der " +
        "Universität eine Personalmanagement Software " +
        "entwickelt. " +
        "Die Anwendung basierte auf Blazor und wurde, " +
        "wie in der Uni üblich, mit \"Lehrbuch\"-Softwareentwicklungsprozessen entwickelt." +
        "Ich übernahm die Rolle des Projektleiters und " +
        "habe dabei sehr viel über die Leitung von Softwareprojekten gelernt, " +
        "was besonders durch das stark unterschiedliche Leistungsniveau im Team herausfordernd war."
  },
  {
    title: "7. Hardwareprojekte",
    technologies: "ESP32, C++, Rust, UWB",
    description:
        "Neben der Web- und Softwareentwicklung interessiere ich " +
        "mich auch für Elektronik. Ich habe Platinen entworfen, selbst gefertigt und mit " +
        "C++ und Rust programmiert. Dies habe ich unter anderem für meine Bachelorarbeit gemacht, die ich " +
        "im Bereich HCI (Human Computer Interaction) absolvierte. In dieser habe ich einen funktionsfähigen " +
        "Prototyp für ein Pflanzenpflegesystem auf UWB- und ESP32-Basis " +
        "entwickelt. Solche Hardwareprojekte verbinden mein Interesse " +
        "an IoT-Lösungen mit einer praktischen Umsetzung in Form " +
        "selbstgebauter Prototypen."
  },
  {
    title: "8. Sonstiges",
    description:
        "Neben den genannten Projekten gibt es noch viele weitere. " +
        "Inzwischen übernehme ich auch im beruflichen Umfeld " +
        "immer mehr leitende Aufgaben und setze Projekte in direkter Kundenabstimmung um."
  }
];
</script>

<template>
  <section id="projects">
    <h2>Projekte</h2>
    <p>{{ introText }}</p>

    <article
        v-for="(project, index) in projects"
        :key="index"
    >
      <h3>{{ project.title }}</h3>
      <p>
        <template v-if="project.technologies">
          <strong>Technologien:</strong>
          {{ project.technologies }}
          <br>
          <strong>Beschreibung:</strong>
        </template>
        {{ project.description }}
      </p>
    </article>
  </section>
</template>

<style scoped>
h2 {
  margin-top: 0;
  color: var(--color-heading);
}

h3 {
  margin-bottom: 0.5rem;
  color: var(--color-heading);
}

article {
  margin-bottom: 2rem;
}

p {
  margin-bottom: 1rem;
  color: var(--color-text);
}
</style>