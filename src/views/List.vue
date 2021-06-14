<template>
  <v-container class="items-list">
    <TopBar/>
    <v-row align="center" justify="space-between" class="px-2">
      <v-col cols="4" class="mt-1">
        <v-text-field
            prepend-inner-icon="mdi-magnify"
            label="Copacabana"
            :value="$route.params.filter.keyword"
            solo
        ></v-text-field>
      </v-col>
      <v-col cols="2">
        <InputText/>
      </v-col>
      <v-col cols="1" class="ml-n9 mr-md-6 mr-lg-0 mr-sm-3">
        <CustomRadio/>
      </v-col>
      <v-col cols="5">
        <SelectChips/>
      </v-col>
    </v-row>
    <v-row align="top">
      <v-col cols="9">
        <ItemsList/>
      </v-col>
      <v-col cols="3">
        <v-card elevation="4" class="mt-3" min-width="370" min-height="300"></v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import TopBar from "@/components/TopBar";
import ItemsList from "@/components/ItemsList";
import InputText from "@/components/InputText";
import CustomRadio from "@/components/CustomRadio";
import SelectChips from "@/components/SelectChips";

  export default {
    name: 'List',
    components: {
      TopBar,
      ItemsList,
      InputText,
      CustomRadio,
      SelectChips
    }
  }
</script>

<style lang="sass">
  .items-list
    display: flex
    flex-direction: column
    margin: 25px
</style>