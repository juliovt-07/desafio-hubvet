<template>
  <v-container class="items-list">
    <TopBar/>
    <v-row align="center">
      <v-col cols="10">
        <ItemsList/>
      </v-col>
      <v-col cols="2">
        <v-card min-width="300" min-height="300"></v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import TopBar from "@/components/TopBar";
import ItemsList from "@/components/ItemsList";

  export default {
    name: 'List',
    components: {
      TopBar,
      ItemsList
    }
  }
</script>

<style lang="sass">
  .items-list
    display: flex
    flex-direction: column
    margin: 25px
</style>