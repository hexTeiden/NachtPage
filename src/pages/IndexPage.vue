<template>
  <q-page class="flex flex-center bg-blue-grey-9 col">
    <div class="wrapper">
      <div class="q-pa-md q-gutter-sm no-wrap col-4" id="banner" name="divs">
        <q-banner
          rounded
          :class="$q.dark.isActive ? 'bg-grey-9' : 'bg-grey-2'"
          style="width: 800px"
        >
          <template v-slot:avatar>
            <img src="./images/3D_Modell.png" style="width: 100px; height: 64px" />
          </template>
          <div class="text-h5">Willkommen zum Projekt "Nachtkastel"</div>
          <div>
            Die Lösung unseres Projektteams wäre einen Nachtkästchen aus alten bereits gebrauchten
            und mittlerweile unbrauchbaren Materialien zu bauen, der Tisch hätte 2 Laden und eine
            Ablagefläche über den Laden, ebenfalls wäre er durch Rollen bewegbar, somit kann man das
            Nachtkästchen überall hinstellen und hat auch für verschiedene Sachen wie Medikamente,
            Ladekabel oder ähnliches eine Ablagefläche.
          </div>
        </q-banner>
      </div>
      <div class="q-pa-md row items-start q-gutter-md" id="cards">
        <q-card class="my-card">
          <q-card-section>
            <div class="text-h5">Projektleiter</div>
          </q-card-section>
          <img src="./images/Matteo.jpg" style="height: 332px" />

          <q-card-section>
            <div class="text-h6">Matteo Knogler</div>
            <div class="text-subtitle2">Alter: 18</div>
            <div class="text-subtitle2">Klasse: 3CHIT</div>
          </q-card-section>
        </q-card>
        <q-card class="my-card">
          <q-card-section>
            <div class="text-h5">Projektmitglied</div>
          </q-card-section>
          <img src="./images/Lukas.jpg" />

          <q-card-section>
            <div class="text-h6">Lukas Ivejic</div>
            <div class="text-subtitle2">Alter: 16</div>
            <div class="text-subtitle2">Klasse: 3CHIT</div>
          </q-card-section>
        </q-card>
        <q-card class="my-card">
          <q-card-section>
            <div class="text-h5">Projektmitglied</div>
          </q-card-section>
          <img src="./images/Sayed.jpeg" />

          <q-card-section>
            <div class="text-h6">Sayed Sadat</div>
            <div class="text-subtitle2">Alter: 18</div>
            <div class="text-subtitle2">Klasse: 3CHIT</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="q-pa-md q-gutter-sm" id="model">
        <Model />
      </div>
      <div class="q-pa-md q-gutter-sm" id="material">
        <Material />
      </div>
      <q-page-sticky position="bottom-right" :offset="[10, 10]" expand>
        <Popup />
      </q-page-sticky>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';
import Popup from 'src/components/Popup.vue';
import Model from 'src/components/Model.vue';
import Material from 'src/components/Material.vue';

export default defineComponent({
  name: 'IndexPage',
  components: { Popup, Model, Material },
});
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px

.wrapper
  display: flex
  flex-direction: column
</style>
