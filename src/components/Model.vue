<template>
  <div class="q-pa-md flex flex-center">
    <q-card class="my-card" flat bordered>
      <q-card-section>
        <div class="text-h6">3D Modell</div>
        <div class="text-subtitle2">
          via
          <a href="https://www.blender.org" target="_blank" style="text-decoration: none"
            >Blender</a
          >
        </div>
      </q-card-section>

      <q-tabs v-model="tab">
        <q-tab label="Image" name="one" />
        <q-tab label="In Software" name="two" />
        <q-tab label="Software" name="three" />
      </q-tabs>

      <q-separator />

      <q-tab-panels v-model="tab" animated>
        <q-tab-panel name="one">
          <q-img
            src="../pages/images/3D_Modell.png"
            :ratio="16 / 9"
            spinner-color="primary"
            spinner-size="82px"
          />
        </q-tab-panel>

        <q-tab-panel name="two">
          <q-img
            src="../pages/images/3D_Modell.png"
            :ratio="16 / 9"
            spinner-color="primary"
            spinner-size="82px"
          />
        </q-tab-panel>

        <q-tab-panel name="three" class="text-black">
          Blender ist eine umfassende 3D-Modellierungssoftware mit zahlreichen Funktionen. Hier sind
          einige der wichtigsten Features zusammengefasst:
          <ul>
            <li>
              Modellierungswerkzeuge: Blender bietet eine Vielzahl von Werkzeugen für die
              Modellierung, darunter Extrusion, Beveling, Sculpting und mehr. Polygonale
              Modellierung und NURBS-Modellierung werden unterstützt.
            </li>
            <li>
              Materialien und Shading: Die Software ermöglicht die Erstellung und Zuweisung von
              Materialien mit fortschrittlichen Shader-Optionen. Physikalisch basierte
              Rendering-Materialien sind verfügbar.
            </li>
            <li>
              Animation: Blender ermöglicht die Erstellung von 3D-Animationen mit Funktionen wie
              Keyframing, Inverse Kinematics (IK), Armaturen und Pfaden. Die Software unterstützt
              auch Partikel- und Flüssigkeitssimulationen.
            </li>
            <li>
              Texturierung und UV-Mapping: Texturierungswerkzeuge ermöglichen die Anwendung von
              Texturen auf Modelle. UV-Mapping wird unterstützt, um Texturen auf Modelle zu
              projizieren.
            </li>
            <li>
              Beleuchtung und Rendering: Blender bietet leistungsstarke Beleuchtungswerkzeuge,
              einschließlich HDR-Beleuchtung und Global Illumination. Fortschrittliche
              Rendering-Engines wie Cycles und Eevee sind integriert.
            </li>
            <li>
              VFX (Visual Effects): Blender enthält Funktionen für die Erstellung von visuellen
              Effekten, einschließlich Rauch, Feuer, Partikel und mehr. Rigid Body und Soft Body
              Simulationen sind ebenfalls verfügbar.
            </li>
            <li>
              Compositing: Die Software verfügt über einen integrierten Node-basierten Compositor
              für Post-Processing-Effekte.
            </li>
            <li>
              Game Development: Blender kann auch für die Erstellung von 3D-Spielen verwendet
              werden. Es bietet Funktionen für das Modellieren von Spielelementen und die
              Integration von Spiellogik.
            </li>
            <li>
              Python-Skripting: Blender ist durch Python-Skripting erweiterbar, was fortgeschrittene
              Anpassungen und Automatisierungen ermöglicht.
            </li>
            <li>
              Open-Source und Community: Blender ist kostenlos und Open-Source. Eine aktive
              Community trägt zur ständigen Weiterentwicklung und Unterstützung bei.
            </li>
          </ul>
          Diese Funktionen machen Blender zu einer vielseitigen 3D-Modellierungssoftware, die von
          Anfängern bis hin zu fortgeschrittenen Anwendern genutzt werden kann.
        </q-tab-panel>
      </q-tab-panels>
    </q-card>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    return {
      tab: ref('one'),
    };
  },
};
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 800px
</style>
