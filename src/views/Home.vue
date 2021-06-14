<template>
  <v-container class="home">
    <v-card class="justify-center transparent" flat>
      <v-row align="center" class="justify-center">
        <v-col cols="4">
          <v-img
            :src="require('../assets/logo.png')"
            class="my-5"
            contain
            height="90"
          />
          <v-text-field
              v-model="filter.keyword"
              prepend-inner-icon="mdi-magnify"
              label="Copacabana"
              class="input"
              height="58"
              solo
          ></v-text-field>
        </v-col>
      </v-row>
      <v-row no-gutters justify="center" align="center">
        <v-col sm="2" lg="2" class="mx-3">
          <SelectDefault @update-select-default="updateSelectDefault"/>
        </v-col>
        <v-col sm="2" lg="2" class="mx-3">
          <InputText @update-city="updateCity"/>
        </v-col>
        <v-col sm="3" lg="1" class="mt-n5 mx-3">
          <CustomRadio label="Milhas ou R$" @update-custom-radio="updateCustomRadio"/>
        </v-col>
        <v-col sm="6" lg="4"  class="mb-1 mx-3">
          <SelectChips @update-select-chips="updateSelectChips"/>
        </v-col>
      </v-row>
      <v-row class="justify-center mb-13">
        <v-col cols="7" md="2" sm="3">
          <v-btn
              color="#44BBA4"
              block
              large
              elevation="2"
              max-width="20"
              height="40"
              tile
              class="white--text"
          >
            <router-link class="text-decoration-none white--text" :to="{ name: 'List', params: { filter: filter } }">
              Pesquisar
            </router-link>
          </v-btn>
        </v-col>
      </v-row>
    </v-card>  
  </v-container>
</template>

<script>
import SelectDefault from "@/components/SelectDefault";
import InputText from "@/components/InputText";
import CustomRadio from "@/components/CustomRadio";
import SelectChips from "@/components/SelectChips";

  export default {
    name: 'Home',
    components: {
      SelectDefault,
      InputText,
      CustomRadio,
      SelectChips
    },
    data: () => ({
      filter: {
        keyword: '',
        type: '',
        city: '',
        valueOrder: '',
        labels: []
      }
    }),
    methods: {
      updateSelectDefault(value) {
        this.filter.type = value
      },
      updateCity(value) {
        this.filter.city = value
      },
      updateCustomRadio(value) {
        this.filter.valueOrder = value
      },
      updateSelectChips(value) {
        this.filter.labels = value
      },
    }
  }
</script>

<style lang="sass">
  .home
    min-height: 100vh
    display: grid
    align-items: center
    .input div
      border-radius: 8px
</style>