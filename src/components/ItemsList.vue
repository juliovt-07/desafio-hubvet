<template>
  <v-container>
    <v-data-table
        :headers="headers"
        :items="destinatios"
        :items-per-page="4"
        class="elevation-1"
        v-model="selected"
        item-key="name"
        show-select
    >
      <template v-slot:item.labels="{ item }">
        <v-row>
          <v-col>
            <svg class="mx-1" v-for="(label, id) in item.labels" :key="label" width="7" height="7" viewBox="0 0 7 7" fill="none" xmlns="http://www.w3.org/2000/svg">
              <circle cx="3.5" cy="3.5" r="3.5" :fill="getColor(item.labels[id])"/>
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
      destinatios: [
        {
          code: 'HP556',
          name: 'Final de ano em Copacabana',
          price: '7.591,70',
          labels: ['promocao', 'novos', 'ultimosdias']
        },
        {
          code: 'HP504',
          name: 'Carnaval em Copacabana',
          price: '6.266,10',
          labels: ['promocao', 'novos', 'ultimosdias']
        },
        {
          code: 'HP556',
          name: 'Feriadão em Copacabana',
          price: '2.190,75',
          labels: ['promocao', 'novos', 'ultimosdias']
        },
        {
          code: 'HP589',
          name: 'Semana Santa em Copacabana',
          price: '3.490,11',
          labels: ['promocao', 'novos', 'ultimosdias']
        },
        {
          code: 'HP511',
          name: 'Final de ano em Copacabana',
          price: '7.591,70',
          labels: ['promocao', 'novos']
        },
        {
          code: 'HP556',
          name: 'Carnaval em Copacabana',
          price: '6.266,10',
          labels: ['promocao', 'ultimosdias']
        },
        {
          code: 'HP511',
          name: 'Feriadão em Copacabana',
          price: '2.190,75',
          labels: ['novos']
        },
        {
          code: 'HP556',
          name: 'Semana Santa em Copacabana',
          price: '3.490,11',
          labels: ['novos', 'ultimosdias']
        },
        {
          code: 'HP504',
          name: 'Final de ano em Copacabana',
          price: '7.591,70',
          labels: ['promocao', 'novos', 'ultimosdias']
        },
        {
          code: 'HP556',
          name: 'Carnaval em Copacabana',
          price: '6.266,10',
          labels: ['ultimosdias']
        },
      ]
    }),
    methods: {
      getColor (calories) {
        if (calories === 'promocao') return '#FF4A4A'
        else if (calories === 'novos') return '#FFA800'
        else if (calories === 'ultimosdias') return '#DB00FF'
      },
    }
  }
</script>

<style lang="sass">

</style>