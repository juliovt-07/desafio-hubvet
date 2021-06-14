<template>
  <v-container class="select-content">
    <span>Buscar por</span>
    <v-select
        v-model="selected"
        class="select-input mt-n5"
        :items="items"
        item-text="label"
        label="Todos"
        single-line
        @change="updateSelectDefault()"
    ></v-select>
  </v-container>
</template>

<script>
  export default {
    name: 'SelectDefault',
    data: () => ({
      selected: '',
      items: [
        { label: 'Todos', value: 'todos' },
        { label: 'Voos', value: 'voos' },
        { label: 'Hotéis', value: 'hoteis' },
        { label: 'Carros', value: 'carros' },
        { label: 'Pacotes', value: 'pacotes' }
      ]
    }),
    methods: {
      updateSelectDefault() {
        this.$emit('update-select-default', this.selected)
      }
    }
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