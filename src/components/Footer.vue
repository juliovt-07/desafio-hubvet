<template>
    <v-row class="footer">
      <v-col col="12">
        <v-card height="150" flat class="transparent">
          <v-footer absolute class="font-weight-regular transparent">
            <v-col class="text-center" cols="12">
              <v-row class="justify-center" align="center">
                <span>Mantido &#38; Feito com</span>
                <svg class="mx-1" width="18" height="16" viewBox="0 0 18 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" clip-rule="evenodd" d="M15.3922 2.15664C14.652 1.41607 13.6478 1 12.6007 1C11.5537 1 10.5495 1.41607 9.80929 2.15664L9.04864 2.91729L8.28798 2.15664C6.74631 0.614965 4.24676 0.614965 2.70508 2.15664C1.16341 3.69832 1.16341 6.19786 2.70508 7.73954L3.46574 8.50019L9.04864 14.0831L14.6315 8.50019L15.3922 7.73954C16.1328 6.99932 16.5488 5.99516 16.5488 4.94809C16.5488 3.90102 16.1328 2.89686 15.3922 2.15664Z" stroke="#F30000" stroke-opacity="0.5" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
                <span>COPYRIGHT &#64; {{ new Date().getFullYear() }}</span>
                <img
                  src="../assets/logo2.png"
                  class="mx-1"
                  alt="logo"
                  height="16"
                >
                <span>, All rights Reserved</span>
              </v-row>
            </v-col>
          </v-footer>
        </v-card>
      </v-col>
    </v-row>
</template>

<script>
  export default {
    name: 'Footer',

    data: () => ({

    }),
  }
</script>

<style lang="sass">
  .footer
    position: absolute
    bottom: 8px
    left: 0px
    right: 0px
    span
      font-size: 10px
      line-height: 13.5px
</style>