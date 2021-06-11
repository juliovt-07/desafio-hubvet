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
          <v-row no-gutters>
            <v-col cols="12" sm="4">
                <SelectDefault/>
            </v-col>
            <v-col cols="12" sm="4">
                <InputText/>
            </v-col>
            <v-col cols="12" sm="4">

            </v-col>
            <v-col cols="12" sm="4">

            </v-col>
          </v-row>
          <v-row class="justify-center">
            <v-col cols="7">
              <v-btn
                color="#44BBA4"
                block
                large
                elevation="2"
                min-width="230"
                height="40"
                tile
                class="white--text"
              >
                Pesquisar
              </v-btn>
            </v-col>
          </v-row>

        </v-col>
      </v-row>
    </v-card>  
  </v-container>
</template>

<script>
import SelectDefault from "@/components/SelectDefault";
import InputText from "@/components/InputText";

  export default {
    name: 'Home',
    components: {
      SelectDefault,
      InputText
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