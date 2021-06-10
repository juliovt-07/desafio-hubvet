<template>
  <v-container>
    <v-data-table
        :headers="headers"
        :items="desserts"
        :items-per-page="4"
        class="elevation-1"
        v-model="selected"
        item-key="name"
        show-select
    ></v-data-table>
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
      desserts: [
        {
          code: 'HP556',
          name: 'Final de ano em Copacabana',
          price: '7.591,70',
          labels: '.'
        },
        {
          code: 'HP504',
          name: 'Carnaval em Copacabana',
          price: '6.266,10',
          labels: '.'
        },
        {
          code: 'HP556',
          name: 'Feriadão em Copacabana',
          price: '2.190,75',
          labels: '.'
        },
        {
          code: 'HP589',
          name: 'Semana Santa em Copacabana',
          price: '3.490,11',
          labels: '.'
        },
        {
          code: 'HP511',
          name: 'Final de ano em Copacabana',
          price: '7.591,70',
          labels: '.'
        },
        {
          code: 'HP556',
          name: 'Carnaval em Copacabana',
          price: '6.266,10',
          labels: '.'
        },
        {
          code: 'HP511',
          name: 'Feriadão em Copacabana',
          price: '2.190,75',
          labels: '.'
        },
        {
          code: 'HP556',
          name: 'Semana Santa em Copacabana',
          price: '3.490,11',
          labels: '.'
        },
        {
          code: 'HP504',
          name: 'Final de ano em Copacabana',
          price: '7.591,70',
          labels: '.'
        },
        {
          code: 'HP556',
          name: 'Carnaval em Copacabana',
          price: '6.266,10',
          labels: '.'
        },
      ]
    }),
  }
</script>

<style lang="sass">

</style>