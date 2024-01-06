<template>
  <div class="bg-blue-grey-10 text-white text-center q-pa-md flex flex-center">
    <div>
      <div><Roadmap /></div>
      <q-btn
        class="q-mt-xl"
        color="primary"
        text-color="white"
        unelevated
        to="/"
        label="Go Home"
        no-caps
      />
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import Roadmap from 'src/components/Roadmap.vue';

export default defineComponent({
  name: 'ErrorNotFound',
  components: {
    Roadmap,
  },
});
</script>
