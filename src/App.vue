<template>
  <v-app id="inspire">
    <SystemBar
      message="Chat with people who come to your websites and social media!" 
      :button="{ to: '/about', color: 'success', show: true }"
      closable
    />
    <!-- <v-navigation-drawer color="grey lighten-3" style="border: 2px solid red;" width="600px" height="110vh" v-model="drawer" app>
      
      <v-navigation-drawer color="grey lighten-4" style="margin:0 0 0 0; width: 300px;" absolute height="110vh" v-model="drawer">
        <IntroSheet style="margin:0 0 0 0; width: 300px;" />

        <PrimarySideList style="margin:0 0 0 0; width: 300px;" />

        <template  style="margin:0 0 0 0; width: 300px;" v-slot:append>
            <v-list class="ma-0">
              <v-list-item link class="ma-0">
                <v-list-item-icon>
                  <v-icon>mdi-logout</v-icon>
                </v-list-item-icon>
                
                <v-list-item-content>
                  <v-list-item-title>Logout</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
        </template>
      </v-navigation-drawer>

      <SecondarySideList style="margin: 0 0 0 300px;" />



    </v-navigation-drawer> -->
    <v-navigation-drawer width="550px" height="110vh" v-model="drawer" app>
      <v-row class="pa-0 ma-0" style="height: 100%;">
        <v-col cols="6" class="pa-0 ma-0 grey lighten-3" style="border-right: 2px solid grey">
          <IntroSheet class="pa-0 ma-0" />

          <PrimarySideList class="pa-0 ma-0" />
        </v-col> 
        <v-col class="pa-0 ma-0 grey lighten-5" cols="6" color="grey darken-1">
          <SecondarySideList class="pa-0 ma-0" />
        </v-col>
      </v-row>
    </v-navigation-drawer>

    <v-main>
      <v-container
        class="my-8 px-6"
        fluid
      >
        <v-main class="pa-0">
          <router-view />
        </v-main>
      </v-container>
    </v-main>

    <Footer />
  </v-app>
</template>
<style>
  #inspire {
    zoom: 90%;
    margin: 0;
    padding: 0;
  }
</style>

<script>
  import SystemBar from './components/Layout/SystemBar.vue'
  import IntroSheet from './components/Layout/IntroSheet.vue'
  import PrimarySideList from './components/Layout/PrimarySideList.vue'
  import SecondarySideList from './components/Layout/SecondarySideList.vue'
  import Footer from './components/Layout/Footer.vue'

  export default {
    name: 'App',
    components: {
      SystemBar,
      IntroSheet,
      PrimarySideList,
      SecondarySideList,
      Footer,
    },
    data: () => ({
      cards: ['Today', 'Yesterday'],
      drawer: null,
      drawerChild: null,
      links: [
        ['mdi-inbox-arrow-down', 'Inbox'],
        ['mdi-send', 'Send'],
        ['mdi-delete', 'Trash'],
        ['mdi-alert-octagon', 'Spam'],
        ['mdi-logout', 'Logout'],
      ],
    }),
  }
</script>


  import HelloWorld from '../components/HelloWorld'

  export default {
    name: 'Home',

  }




