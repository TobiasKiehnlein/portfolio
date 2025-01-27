<script setup lang="ts">

</script>

<template>
  <section id="about" class="grid horizontal high-contrast">
    <h2>Über mich</h2>
    <div>
      <p class="tldr">tl;dr: Ich programmiere seit ich denken kann und liebe es Zeug zu automatisieren.</p>
      <div>
        <p>
          Seit ich denken kann, fasziniert mich die Softwareentwicklung.
          Meine ersten Schritte machte ich mit <b>Python</b> in
          <b>Blender</b>, wo ich einfache Spiele mit der
          <b>Blender Game Engine</b> entwickelte. Bald darauf entdeckte
          ich die App-Entwicklung für mich und programmierte meine ersten mobilen
          Anwendungen mit <b>Java</b>.
        </p>

        <p>
          Meine Begeisterung für Spiele brachte mich schließlich zu
          <b>Unity</b>, wo ich mich – unter anderem durch die Teilnahme an
          <b>Game Jams</b> – intensiv einarbeitete. In der 11. Klasse
          entwickelte ich im Rahmen meines P-Seminars meine erste „große“ App, die
          schließlich sowohl im <b>Google Play Store</b> als auch im
          <b>Apple App Store</b> veröffentlicht wurde. Diese mit
          <b>React Native</b> und <b>Expo</b> entwickelte
          Anwendung diente als umfassende Schul-App zur Verwaltung von
          Vertretungsplänen, Hausaufgaben und Stundenausfällen.
          Durch die Zusammenarbeit mit <strong>Fujitsu</strong> führte dieses Projekt
          unter anderem zum Gewinn des <strong>SCHULEWIRTSCHAFTPREISES 2018</strong>.
        </p>

        <p>
          Direkt nach der Schule begann ich meine Tätigkeit als Softwareentwickler
          bei <b>CubeFour</b>, wo ich mich verstärkt auf die
          <b>Webentwicklung</b> konzentrierte. Im Laufe der Zeit habe ich
          mit einer Vielzahl moderner Technologien gearbeitet, darunter
          <b>AngularJS, ASP.NET MVC, Angular, React, Vue.js</b>,
          <b>Node.js</b> und viele mehr.
        </p>

        <p>
          Mit wachsenden Projektanforderungen verlagerte sich mein Fokus zunehmend
          auf <b>DevOps</b> und CI/CD. Ich habe mich intensiv mit
          Technologien wie <b>Docker, GitLab CI/CD, GitHub Actions, Ansible</b>
          und weiteren Tools auseinandergesetzt, um Entwicklungs- und
          Deploymentprozesse effizienter zu gestalten.
        </p>

        <p>
          <b>Auch privat setze ich kontinuierlich Projekte um, um mich weiterzuentwickeln.</b>
          Mein Zuhause wird über <b>Homeassistant</b> gesteuert, erweitert
          durch zahlreiche selbst geschriebene Programme, die via <b>REST</b>-
          und <b>WebSocket</b>-APIs, <b>NodeRED</b> und weiteren
          Schnittstellen miteinander kommunizieren. Aktuell arbeite ich zudem an einer
          App zur Verwaltung von Einkaufslisten, die aus vergangenen Käufen lernt und
          künftige Listen intelligent sortiert, um ein möglichst effizientes
          Einkaufserlebnis zu schaffen.
        </p>

        <p>
          Mehr Details zu den einzelnen Projekten sind weiter unten zu finden.
        </p>

        <p>
          Parallel zu meiner beruflichen Tätigkeit habe ich Informatik an der
          <b>Universität Augsburg</b> studiert, um mein praxisbezogenes
          Wissen durch fundierte theoretische Grundlagen zu ergänzen.
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">

.grid {
  display: grid;
  gap: 20px;

  p {
    color: var(--color-text);
    margin-bottom: 20px;

    b, &.tldr {
      font-weight: bold;
    }
  }

}
</style>