<template>
  <v-app class="app">
    <v-main>
      <router-view class="content"/>
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import Footer from '@/components/Footer'

export default {
  name: 'App',
  components: {
    Footer
  },
  data: () => ({
    //
  }),
};
</script>

<style lang="sass">
  div[data-app='true']
    font-family: 'Poppins', sans-serif
    min-height: 90vh
    min-width: 90vw
    overflow: hidden
</style>