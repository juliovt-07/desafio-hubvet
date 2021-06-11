<template>
  <v-container class="select-chips-content">
    <span class="label">Etiquetas</span>
    <v-select
        v-model="selected"
        class="select-chips mt-n5"
        :items="items"
        item-text="label"
        chips
        multiple
        single-line
    >
      <template v-slot:selection="{ item }">
        <v-chip
            small
            close
            outlined
            @click:close="removeItem(item.value)"
            :color="colorLabels(item.value)"
        >
          {{item.label}}
        </v-chip>
      </template>
    </v-select>
  </v-container>
</template>
<script>
  export default {
    name: 'SelectChips',
    data: () => ({
      selected: [],
      items: [
        { label: 'Promoção', value: 'promocao' },
        { label: 'Novos', value: 'novos' },
        { label: 'Ultimos Dias', value: 'ultimosdias' }
      ]
    }),
    methods: {
      colorLabels(label) {
        if (label === 'promocao') return '#FF4A4A'
        else if (label === 'novos') return '#FFA800'
        else if (label === 'ultimosdias') return '#DB00FF'
      },
      removeItem(value) {
        this.selected.splice(this.selected.indexOf(value), 1);
      }
    }
  }
</script>

<style lang="sass">
  .select-chips-content .label
    font-size: 10px
    color: #909CA7
  .select-chips label, .v-select__selection
    font-size: 12px
</style>