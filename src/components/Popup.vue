<template>
  <div class="q-pa-md">
    <q-btn color="blue-10" @click="showNotif" label="Click Me" />
  </div>
</template>

<script>
import { useQuasar } from 'quasar';

export default {
  setup() {
    const $q = useQuasar();

    return {
      showNotif() {
        $q.notify({
          progress: true,
          message: 'Nicht vergessen das Projekt zu bewerten :D',
          color: 'primary',
          multiLine: true,
          avatar:
            'https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/Infobox_info_icon.svg/1200px-Infobox_info_icon.svg.png',
        });
      },
    };
  },
};
</script>
