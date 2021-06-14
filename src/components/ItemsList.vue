<template>
  <v-container>
    <v-tabs
      background-color="rgba(0, 0, 0, 0.0)"
      color="#44BBA4"
      v-model="activeTab"
    >
      <v-tab
        v-for="(tab, index) in tabs"
        :key="index"
      >
        {{ tab.label }}
      </v-tab>
    </v-tabs>
    <v-data-table
        v-for="(table, index) in tables"
        :key="index"
        :headers="table.headers"
        :items="table.packages"
        :items-per-page="4"
        class="elevation-4"
        v-model="table.selected"
        item-key="name"
        v-show="activeTab === table.id"
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
      activeTab: '',
      tabs: [
        { label: 'Passagens', value: 'passagens' },
        { label: 'Hotéis', value: 'hoteis' },
        { label: 'Carros', value: 'carros' },
        { label: 'Pacotes', value: 'pacotes' },
      ],
      tables: {
        passages: {
          id: 0,
          selected: [],
          headers: [
            {
              align: 'start',
              sortable: false,
            },
            {text: 'Código', value: 'code'},
            {text: 'Origem', value: 'origin'},
            {text: 'Destino', value: 'destiny'},
            {text: 'Milhas', value: 'miles'},
            {text: 'Etiquetas', value: 'labels'}
          ],
          packages: require('../data/passages.json')
        },
        hotels: {
          id: 1,
          selected: [],
          headers: [
            {
              align: 'start',
              sortable: false,
            },
            {text: 'Código', value: 'code'},
            {text: 'Cidade', value: 'city'},
            {text: 'Preço', value: 'price'},
            {text: 'Etiquetas', value: 'labels'}
          ],
          packages: require('../data/hotels.json')
        },
        cars: {
          id: 2,
          selected: [],
          headers: [
            {
              align: 'start',
              sortable: false,
            },
            {text: 'Código', value: 'code'},
            {text: 'Cidade', value: 'city'},
            {text: 'Preço', value: 'price'},
            {text: 'Etiquetas', value: 'labels'}
          ],
          packages: require('../data/hotels.json')
        },
        packages: {
          id: 3,
          selected: [],
          headers: [
            {
              align: 'start',
              sortable: false,
            },
            {text: 'Código', value: 'code'},
            {text: 'Nome', value: 'name'},
            {text: 'Preço (R$)', value: 'price'},
            {text: 'Etiquetas', value: 'labels'}
          ],
          packages: require('../data/packages.json')
        }
      }
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