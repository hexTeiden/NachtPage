<template>
  <q-page class="flex flex-center bg-blue-grey-9">
    <div class="q-pa-md q-gutter-sm" id="banner">
      <q-banner rounded :class="$q.dark.isActive ? 'bg-grey-9' : 'bg-grey-2'" style="width: 700px">
        <template v-slot:avatar>
          <img src="./images/3D_Modell.png" style="width: 100px; height: 64px" />
        </template>
        <div class="text-h5">Willkommen zum Projekt "Nachtkastel"</div>
        <div>
          Das Projekt "Nachtkastel" ist ein Nachtkasten welcher aus gebrauchten Materialien
          zusammengebaut wurde. <br />
        </div>
      </q-banner>
    </div>
    <div class="q-pa-md row items-start q-gutter-md" id="cards">
      <q-card class="my-card bg-blue-grey-10 text-white">
        <img src="./images/Matteo.png" />

        <q-card-section>
          <div class="text-h6">Matteo Knogler</div>
          <div class="text-subtitle2">Rolle: Projektleiter</div>
        </q-card-section>
      </q-card>
      <q-card class="my-card bg-blue-grey-10 text-white">
        <img src="./images/Matteo.png" />

        <q-card-section>
          <div class="text-h6">Lukas Ivejic</div>
          <div class="text-subtitle2">Rolle: Projektmitglied</div>
        </q-card-section>
      </q-card>
      <q-card class="my-card bg-blue-grey-10 text-white">
        <img src="./images/Matteo.png" />

        <q-card-section>
          <div class="text-h6">Sayed Sadat</div>
          <div class="text-subtitle2">Rolle: Projektmitglied</div>
        </q-card-section>
      </q-card>
    </div>
    <div class="q-pa-md q-gutter-sm">
      <Model />
    </div>
    <div class="q-pa-md q-gutter-sm">
      <Material />
    </div>
    <q-page-sticky position="bottom-right" :offset="[10, 10]" expand>
      <Popup />
    </q-page-sticky>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';
import Popup from 'src/components/Popup.vue';
import Model from 'src/components/Model.vue';
import Material from 'src/components/Model.vue';

export default defineComponent({
  name: 'IndexPage',
  components: { Popup, Model, Material },
});
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>
