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
              prepend-inner-icon="mdi-magnify"
              label="Copacabana"
              class="input"
              height="58"
              solo
          ></v-text-field>
        </v-col>
      </v-row>
      <v-row no-gutters justify="center" align="center">
        <v-col cols="6" sm="4" lg="2">
          <SelectDefault/>
        </v-col>
        <v-col cols="6" sm="4" lg="2">
          <InputText/>
        </v-col>
        <v-col cols="4" sm="3" lg="2">

        </v-col>
        <v-col cols="6" sm="5" lg="4">
          <SelectChips class="mb-1"/>
        </v-col>
      </v-row>
      <v-row class="justify-center mb-10">
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
            Pesquisar
          </v-btn>
        </v-col>
      </v-row>
    </v-card>  
  </v-container>
</template>

<script>
import SelectDefault from "@/components/SelectDefault";
import InputText from "@/components/InputText";
import SelectChips from "@/components/SelectChips";

  export default {
    name: 'Home',
    components: {
      SelectDefault,
      InputText,
      SelectChips
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