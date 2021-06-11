<template>
  <v-container class="select-content">
    <span>Buscar por</span>
    <v-select
        class="select-input mt-n5"
        :items="items"
        label="Todos"
        single-line
    ></v-select>
  </v-container>
</template>

<script>
  export default {
    name: 'SelectDefault',

    data: () => ({
      items: ['Todos', 'Voos', 'Hotéis', 'Carros', 'Pacotes']
    }),
  }
</script>

<style lang="sass">
  .select-content span
    font-size: 10px
    color: #909CA7
  .select-input label, .v-select__selection
    font-size: 12px
    margin-left: 18px
    color: #828282
  .select-input .v-select__selections
    padding-left: 20px
</style>