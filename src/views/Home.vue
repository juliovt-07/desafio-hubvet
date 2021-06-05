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
              solo
          ></v-text-field>
          <v-row class="justify-center">
            <v-col cols="6">
              <v-btn
                  tile
                  color="success"
                  class="py-4 px-10 mx-auto"
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

  export default {
    name: 'Home'
  }
</script>

<style lang="sass">
  .home
    min-height: 100vh
    display: grid
    align-items: center
    .input div
      padding: 11px
      border-radius: 8px
</style>