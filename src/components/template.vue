<template>
  <v-system-bar v-if="show" app>
    <v-spacer/>
    
    <span v-text="message" />
    
    <v-btn
      class="ms-3 px-3 py-0"
      x-small
      :show="button.show"
      :to="button.to"
      :color="button.color"
      dark
    >
      Explore
    </v-btn>

    <v-spacer/>

      <v-btn
        icon
        x-small
        class="ps-1"
        v-show="closable"
        @click="show = false"
      >
        <v-icon>mdi-close</v-icon>
      </v-btn>
    

  </v-system-bar>
</template>

<script>
  export default {
    name: 'SystemBar',
    props: {
      message: { type: String, required: true }, 
      button: { type: Object, required: true },
      closable: { type: Boolean, default: false },
    },
    data: () => ({
      show: true
    }),
    methods: {
      fetch() {
        console.log("FETCH FIRED", {message: this.message, button: this.button})
      }
    },
    mounted() {
      this.fetch();
    }
  }
</script>
