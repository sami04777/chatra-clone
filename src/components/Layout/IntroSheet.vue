<template>
  <v-sheet 
    color="grey lighten-4"
    class="pa-0"
  >
    <v-row class="px-4 pt-4 pb-0">
      <v-col cols="3">
        <v-badge avatar top color="online ? green : grey accent-4" offset-x="19" offset-y="15">
          <v-avatar size="64">
            <v-img src="https://cdn.vuetifyjs.com/images/lists/2.jpg"/>
          </v-avatar>
        </v-badge>
      </v-col>
      
      <v-col class="ps-7" cols="9">
          <h1 class="my-0">John Doe</h1>
          <p class="my-0">john@doe.com</p>
      </v-col>
    </v-row>

      <v-container class="py-0">
        <v-select 
          v-model="status"
          :items="statuses"
          item-text="text"
          item-value="value"
          label="Status"
          return-object
          single-line  
        />
      </v-container>
    <v-row class="pa-0 ma-0">
      <v-bottom-navigation
        background-color="primary"
        dark
        horizontal
        shift
      >
        
        <v-btn class="v-btn-sheet-nav ma-0 pa-0">
          <span>Messages</span>
          <v-icon class="mx-auto">mdi-message</v-icon>
        </v-btn>
        <v-btn class="v-btn-sheet-nav ma-0 pa-0">
          <span>Music</span>
          <v-icon class="mx-auto">mdi-contacts</v-icon>
        </v-btn>
        <v-btn class="v-btn-sheet-nav ma-0 pa-0">
          <span>Book</span>
          <v-icon class="mx-auto">mdi-cog</v-icon>
        </v-btn>
        <v-btn class="v-btn-sheet-nav ma-0 pa-0">
          <span>Status</span>
          <v-icon class="mx-auto">mdi-arrow-down</v-icon>
        </v-btn>
      
      </v-bottom-navigation>
    </v-row>
  </v-sheet>
</template>


<style scoped>
  .v-btn-sheet-nav > small {
    border: 2px solid red;
    text-align: center;
  }
  .v-btn-sheet-nav {
    zoom: 80%;
  }
</style>

<script>
  export default {
    name: 'IntroSheet',
    props: {
      // message: { type: String, required: true }, 
      // button: { type: Object, required: true },
      closable: { type: Boolean, default: false },
    },
    data: () => ({
      show: true,
      status: true,
      statuses: [
        {text: "Online", value: "online"},
        {text: "Offline", value: "offline"},
        {text: "Do Not Disturb", value: "do-not-disturb"},
        {text: "Away", value: "away"},
      ],
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

