<template>
  <v-container class="text-content">
    <span>Onde você está?</span>
    <v-text-field
        class="text-input mt-n5"
        label="Cidade"
        v-model="city"
        @change="updateCity"
        single-line
    ></v-text-field>
  </v-container>
</template>

<script>
  export default {
    name: 'InputText',
    data: () => ({
      city: ''
    }),
    methods: {
      updateCity() {
        this.$emit('update-city', this.city)
      }
    }
  }
</script>

<style lang="sass">
  .text-content span
    font-size: 10px
    color: #909CA7
  .text-input
    input, label
      font-size: 12px
      padding-left: 18px
      color: #828282
    input:focus
      color: #828282
</style>