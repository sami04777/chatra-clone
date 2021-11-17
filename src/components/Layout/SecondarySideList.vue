<template>
 
      <v-list>
        <v-list-item
          v-for="[icon, text] in links"
          :key="icon"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
</template>


<style scoped>
  
</style>

<script>
  export default {
    name: 'SecondarySideList',
    // props: {
    //   closable: { type: Boolean, default: false },
    // },
    data: () => ({
      content: "agent",
      cards: ['Today', 'Yesterday'],
      drawer: null,
      links: [
        ['mdi-inbox-arrow-down', 'Inbox'],
        ['mdi-send', 'Send'],
        ['mdi-delete', 'Trash'],
        ['mdi-alert-octagon', 'Spam'],
      ],
    }),
    // methods: {
    //   fetch() {
    //     console.log("FETCH FIRED", {message: this.message, button: this.button})
    //   }
    // },
    // mounted() {
    //   this.fetch();
    // }
  }
</script>

