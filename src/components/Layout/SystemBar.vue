<template>
  <v-system-bar height="35" v-if="show" app>
    <v-spacer/>
    
    <span v-text="message" />
    
    <v-btn
      class="ms-3 px-3 py-0"
      :show="button.show"
      :to="button.to"
      :color="button.color"
      x-small
    >
      Explore
    </v-btn>

    <v-spacer />

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
  }
</script>
