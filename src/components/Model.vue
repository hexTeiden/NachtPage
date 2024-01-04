<template>
  <div class="q-pa-md">
    <q-card class="my-card" flat bordered>
      <q-card-section>
        <div class="text-h6">3D Modell</div>
        <div class="text-subtitle2">
          via <a href="https://www.blender.org" target="_blank">Blender</a>
        </div>
      </q-card-section>

      <q-tabs v-model="tab" class="text-teal">
        <q-tab label="Tab one" name="one" />
        <q-tab label="Tab two" name="two" />
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
          Blender ist ein 3D Modelling Tool, welcher für Animationen/3D Images verwendet werden
          kann, es bietet eine Vielfalt an Built-In Tools, welche Out of the box verwendet werden
          können.
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
  max-width: 250px
</style>
