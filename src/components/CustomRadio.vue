<template>
  <v-container class="custom-radio-content">
    <span>{{ label }}</span>
      <div class="custom-radios mt-n1">
        <input class="d-none" type="radio" name="valueOrder" id="radio-1" />
        <label for="radio-1" @click="radioSelect('milhas')">
          <svg :width="svgSize" :height="svgSize" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M12.5 3.33337C14.2681 3.33337 15.9638 4.03575 17.214 5.286C18.4643 6.53624 19.1667 8.23193 19.1667 10C19.1667 11.7682 18.4643 13.4638 17.214 14.7141C15.9638 15.9643 14.2681 16.6667 12.5 16.6667C10.7319 16.6667 9.0362 15.9643 7.78595 14.7141C6.53571 13.4638 5.83333 11.7682 5.83333 10C5.83333 8.23193 6.53571 6.53624 7.78595 5.286C9.0362 4.03575 10.7319 3.33337 12.5 3.33337ZM12.5 15C13.8261 15 15.0979 14.4733 16.0355 13.5356C16.9732 12.5979 17.5 11.3261 17.5 10C17.5 8.67396 16.9732 7.40219 16.0355 6.46451C15.0979 5.52682 13.8261 5.00004 12.5 5.00004C11.1739 5.00004 9.90215 5.52682 8.96447 6.46451C8.02678 7.40219 7.5 8.67396 7.5 10C7.5 11.3261 8.02678 12.5979 8.96447 13.5356C9.90215 14.4733 11.1739 15 12.5 15ZM2.5 10C2.5 12.175 3.89167 14.025 5.83333 14.7084V16.45C2.95833 15.7084 0.833334 13.1084 0.833334 10C0.833334 6.89171 2.95833 4.29171 5.83333 3.55004V5.29171C3.89167 5.97504 2.5 7.82504 2.5 10Z" fill="#717172" />
          </svg>
        </label>
        <input class="d-none" type="radio" name="valueOrder" id="radio-2" checked="checked"/>
        <label for="radio-2" @click="radioSelect('dinheiro')">
          <svg :width="svgSize" :height="svgSize" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M5 13.0556H7C7 14.1556 8.37 15.0926 10 15.0926C11.63 15.0926 13 14.1556 13 13.0556C13 11.9352 11.96 11.5278 9.76 10.988C7.64 10.4482 5 9.77597 5 6.94448C5 5.12134 6.47 3.57319 8.5 3.05374V0.833374H11.5V3.05374C13.53 3.57319 15 5.12134 15 6.94448H13C13 5.84448 11.63 4.90745 10 4.90745C8.37 4.90745 7 5.84448 7 6.94448C7 8.06486 8.04 8.47226 10.24 9.01208C12.36 9.55189 15 10.2241 15 13.0556C15 14.8787 13.53 16.4269 11.5 16.9463V19.1667H8.5V16.9463C6.47 16.4269 5 14.8787 5 13.0556Z" fill="#42B29C" />
          </svg>
        </label>
      </div>
  </v-container>
</template>

<script>
  export default {
    name: 'CustomRadio',
    props: {
      label: {
        type: String,
        required: false
      }
    },
    data: () => ({
      radioSelected: null,
      svgSize: 20
    }),
    methods: {
      radioSelect(value) {
        this.radioSelected = value
      }
    },
    watch: {
      radioSelected(value) {
        this.$emit('update-custom-radio', value)
      }
    }
  }
</script>

<style lang="sass">
  .custom-radio-content span
    font-size: 10px
    color: #909CA7
  /* custom-radios STYLING */
  .custom-radios
    display: flex
    justify-content: flex-start
    .custom-radio-content .custom-radios input
      display: none
    label
      cursor: pointer
      padding: 4px 11px
      box-sizing: border-box
      position: relative
      display: inline-block
      border: solid 1px #ddd
      line-height: 140%
      transition: border-color 0.15s ease-out, color 0.25s ease-out, background-color 0.15s ease-out
      &:first-of-type
        border-radius: 4px 0 0 4px
        border-right: none
      &:last-of-type
        border-radius: 0 4px 4px 0
        border-left: none
    input:hover + label
      border-color: #979797
    input:checked + label
      background-color: rgba(68, 187, 164, 0.15)
      color: #fff
      border-color: #44BBA4
      z-index: 1
</style>