<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="bg-dark">
        <q-btn flat dense round icon="menu" aria-label="Menu" @click="toggleLeftDrawer" />
        <q-toolbar-title> Nachtkastel </q-toolbar-title>

        <div>Host: Knogler Matteo</div>

        <q-btn flat dense round icon="menu">
          <q-menu>
            <q-list style="min-width: 100px">
              <q-item clickable class="text-black" @click="scrollbanner">
                <q-item-section>Nachtkastel</q-item-section>
              </q-item>
              <q-item clickable class="text-black" @click="scrollcards">
                <q-item-section>Projektteam</q-item-section>
              </q-item>
              <q-item clickable class="text-black" @click="scroll3d">
                <q-item-section>3D Modell</q-item-section>
              </q-item>
              <q-item clickable class="text-black" @click="scrollmaterial">
                <q-item-section>Materialliste</q-item-section>
              </q-item>
            </q-list>
          </q-menu>
        </q-btn>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered class="bg-dark text-white">
      <q-list class="text-white">
        <q-item-label header> Important Links </q-item-label>

        <EssentialLink v-for="link in essentialLinks" :key="link.title" v-bind="link" />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue';
import EssentialLink from 'components/EssentialLink.vue';

const linksList = [
  {
    title: 'School',
    icon: 'school',
    link: 'https://www.htlwienwest.at',
  },
  {
    title: 'Github',
    icon: 'code',
    link: 'https://github.com/hexTeiden/NachtPage',
  },
  {
    title: 'Google Drive',
    icon: 'code',
    link: 'https://drive.google.com/drive/u/1/folders/1yhL-wdOVhkSTPcLWzdt-2e4JwiBkqxiV',
  },
  {
    title: 'Vue Framework',
    icon: 'public',
    link: 'https://vuejs.org',
  },
  {
    title: 'Quasar Framework',
    icon: 'public',
    link: 'https://quasar.dev',
  },
  {
    title: 'Blender',
    icon: 'public',
    link: 'https://www.blender.org',
  },
];

export default defineComponent({
  name: 'MainLayout',
  methods: {
    scrollbanner() {
      const banner = document.querySelector('#banner');
      banner.scrollIntoView();
    },
    scrollcards() {
      const cards = document.querySelector('#cards');
      cards.scrollIntoView();
    },
    scroll3d() {
      const model = document.querySelector('#model');
      model.scrollIntoView();
    },
    scrollmaterial() {
      const material = document.querySelector('#material');
      material.scrollIntoView();
    },
  },
  components: {
    EssentialLink,
  },
  setup() {
    const leftDrawerOpen = ref(false);

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
