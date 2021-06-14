<template>
  <v-container>
    <v-data-table
        :headers="headers"
        :items="packages"
        :items-per-page="4"
        class="elevation-4"
        v-model="selected"
        item-key="name"
        show-select
    >
      <template v-slot:item.labels="{ item }">
        <v-row>
          <v-col>
            <svg class="mx-1" v-for="(label, id) in item.labels" :key="label" width="7" height="7" viewBox="0 0 7 7" fill="none" xmlns="http://www.w3.org/2000/svg">
              <circle cx="3.5" cy="3.5" r="3.5" :fill="colorLabels(item.labels[id])"/>
            </svg>
          </v-col>
        </v-row>
      </template>
    </v-data-table>
  </v-container>
</template>

<script>
  export default {
    name: 'TopBar',

    data: () => ({
      selected: [],
      headers: [
        {
          align: 'start',
          sortable: false,
        },
        { text: 'Código', value: 'code' },
        { text: 'Nome', value: 'name' },
        { text: 'Preço (R$)', value: 'price' },
        { text: 'Etiquetas', value: 'labels' }
      ],
      packages: require('../data/packages.json')
    }),
    methods: {
      colorLabels (label) {
        if (label === 'promocao') return '#FF4A4A'
        else if (label === 'novos') return '#FFA800'
        else if (label === 'ultimosdias') return '#DB00FF'
      },
    }
  }
</script>

<style lang="sass">

</style>