<template>
  <v-container>
    <v-app-bar
        absolute
        flat
        color="#FFF"
        dense
        class="px-3"
    >
      <img src="../assets/logo.png" alt="logo" id="logo" class="ml-n16">

      <v-spacer></v-spacer>

      <svg class="mr-2" :width="svgSize" :height="svgSize" viewBox="0 0 46 46" fill="none" xmlns="http://www.w3.org/2000/svg">
        <mask id="mask0" mask-type="alpha" maskUnits="userSpaceOnUse" x="0" y="0" width="46" height="46">
          <ellipse cx="23" cy="23" rx="23" ry="23" fill="#E5E5E5"/>
        </mask>
        <g mask="url(#mask0)">
          <mask id="mask1" mask-type="alpha" maskUnits="userSpaceOnUse" x="0" y="0" width="46" height="46">
            <ellipse cx="23" cy="23" rx="23" ry="23" fill="#E5E5E5"/>
          </mask>
          <g mask="url(#mask1)">
            <rect width="46" height="46" fill="#44BBA4"/>
            <path
                d="M30.35 24.4C30.35 25.366 29.566 26.15 28.6 26.15C27.634 26.15 26.85 25.366 26.85 24.4C26.85 23.434 27.634 22.65 28.6 22.65C29.566 22.65 30.35 23.434 30.35 24.4ZM37 23C37 30.7 30.7 37 23 37H9V23C9 15.3 15.3 9 23 9C30.7 9 37 15.3 37 23ZM16 31.4C17.974 33.122 20.2 34.2 23 34.2C29.174 34.2 34.2 29.174 34.2 23C34.2 21.894 34.032 20.83 33.738 19.836C32.73 20.074 31.68 20.2 30.588 20.2C27.788 20.2 25.198 19.36 23 17.946C23 17.946 20.956 25.464 17.442 24.4C16.518 24.12 16 24.834 16 25.8" fill="white"
            />
          </g>
        </g>
      </svg>

    </v-app-bar>
  </v-container>
</template>

<script>
  export default {
    name: 'TopBar',

    data: () => ({
      imgSize: 100,
      svgSize: 35
    }),
  }
</script>

<style lang="sass">
#logo
  transform: scale(0.4)
</style>