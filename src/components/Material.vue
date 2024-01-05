<template>
  <div class="q-pa-md">
    <q-card class="my-card bg-blue-grey-10 text-white" flat bordered>
      <q-card-section>
        <div class="text-h6">Materialliste</div>
        <div class="text-subtitle2">by Matteo Knogler</div>
      </q-card-section>

      <q-markup-table class="bg-blue-grey-10 text-white">
        <thead>
          <tr>
            <th class="text-left">Material</th>
            <th class="text-right">Anzahl</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="text-left">Holzplatten</td>
            <td class="text-right">7</td>
          </tr>
          <tr>
            <td class="text-left">Schrauben</td>
            <td class="text-right">14</td>
          </tr>
          <tr>
            <td class="text-left">Rollen</td>
            <td class="text-right">4</td>
          </tr>
        </tbody>
      </q-markup-table>
    </q-card>
  </div>
</template>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 800px
</style>
