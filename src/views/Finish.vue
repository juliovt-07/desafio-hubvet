<template>
  <v-container class="finish">
    <v-card
      flat
      class="mx-auto card rounded-xl justify-center"
      max-width="400"
      min-height="440"
    >
      <v-container>
        <v-row class="justify-center py-7">
          <img
            :src="require('../assets/logo.png')"
            class="my-3"
            alt="logo"
            height="80"
          />
          <v-card-text class="text-center font-weight-medium">
            <p>Obrigado!</p>
          </v-card-text>
          <v-card-text class="text-center font-weight-medium">
            <p class="black--text">Desejamos uma boa viagem para</p>
            <h6>Copacabana</h6>
          </v-card-text>
        </v-row>
      </v-container>
    </v-card>  
  </v-container>
</template>

<script>

  export default {
    name: 'Finish'
  }
</script>

<style lang="sass">
  #app
    min-width: 100vw
    min-height: 100vh
    background: url('../assets/bg-finish.png') no-repeat center center fixed !important
    background-size: cover !important
    .card
      background: rgba(255, 255, 255, 0.9)
      .card-content
        display: grid
        grid-template-columns: auto
        gap: 60px
        align-items: center
        justify-content: space-between
      .logo
        position: relative
        display: grid
        grid-template-columns: auto
        figcaption
          font-family: 'Roboto Slab', serif
          text-align: right
          position: absolute
          right: 0
          bottom: 14px
          font-size: 18px
          color: #44BBA4
      .text-center
        font-size: 20px
        color: #44BBA4
      .black--text
        opacity: 0.7
      h6
        font-size: 26px
</style>