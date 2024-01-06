<template>
  <div class="q-pa-lg">
    <q-timeline :layout="layout" :side="side" color="secondary">
      <q-timeline-entry heading>Meilenstein Roadmap</q-timeline-entry>

      <q-timeline-entry title="Projektstart" subtitle="9 November 2023" side="left" icon="done_all">
        <div>Start des Projektes.</div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Dokumente/Plannung fertig"
        subtitle="23 November 2023"
        side="right"
        icon="done_all"
      >
        <div>Dokumente fertiggestellt und Plannung abgeschlossen.</div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Projektende"
        subtitle="25 Jänner 2024"
        side="left"
        icon="construction"
        color="orange"
      >
        <div>Projekt wurde beendet und die Technische Abnahme wurde durchgeführt.</div>
      </q-timeline-entry>

      <!-- Website Part der Roadmap -->

      <q-timeline-entry heading>Website</q-timeline-entry>

      <q-timeline-entry title="Wireframe" subtitle="24 November 2023" side="left" icon="done_all">
        <div>Wireframe wurde erstellt und die Struktur der Website wurde festgelegt.</div>
      </q-timeline-entry>

      <q-timeline-entry title="Mockup" subtitle="27 November 2023" side="right" icon="done_all">
        <div>
          Mockup wurde erstellt und die Farben und das Design der Website wurden festgelegt.
        </div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Beginn der Website"
        subtitle="1 Dezember 2023"
        side="left"
        icon="done_all"
      >
        <div>Erster Aufbau der Website wurde begonnen und die ersten Seiten wurden erstellt.</div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Fertigstellung der Website"
        subtitle="6 Jänner 2024"
        side="right"
        icon="done_all"
      >
        <div>Website wurde fertiggestellt und alle Seiten wurden erstellt.</div>
      </q-timeline-entry>

      <q-timeline-entry title="Präsentation" subtitle="9 Jänner 2024" side="left" icon="done_all">
        <div>
          Die Website wurde präsentiert und die Dokumentation wurde abgegeben. Das Projekt wurde
          somit beendet.
        </div>
      </q-timeline-entry>

      <!-- Nachtkasten Part der Roadmap -->

      <q-timeline-entry heading>Nachtkasten</q-timeline-entry>

      <q-timeline-entry title="3D Modell" subtitle="23 November 2023" side="left" icon="done_all">
        <div>3D Modell wurde erstellt und wird als Richtlinie verwendet.</div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Organisation aller Teile"
        subtitle="30 November 2023"
        side="right"
        icon="done_all"
      >
        <div>
          Alle Teile, welche für den Nachtkasten benötigt werden wurden organisiert und in der
          Schule gelagert.
        </div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Beginn der Zusammenbaus"
        subtitle="1 Dezember 2023"
        side="left"
        icon="done_all"
      >
        <div>Der Aufbau des Nachtkastens wurde begonnen.</div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Fertigstellung des Nachtkastens"
        subtitle="8 Jänner 2024"
        side="right"
        icon="done_all"
      >
        <div>Der Nachtkasten wurde fertiggestellt und ist bereit präsentiert zu werden.</div>
      </q-timeline-entry>

      <q-timeline-entry title="Präsentation" subtitle="9 Jänner 2024" side="left" icon="done_all">
        <div>
          Der Nachtkasten wurde präsentiert und die Dokumentation wurde abgegeben. Das Projekt wurde
          somit beendet.
        </div>
      </q-timeline-entry>
    </q-timeline>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    return {
      layout: ref('loose'),
      side: ref('right'),
    };
  },
};
</script>
