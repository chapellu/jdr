<template>
  <v-app>
    <v-container fluid grid-list-md>
      <v-layout row wrap>
        <v-flex d-flex md12>
          <v-card color=purple dark>
            <v-container fluid grid-list-md>
              <v-layout row align-center justify-center>
                <v-flex d-flex md4 >
                  <v-avatar tile size=256>
                    <img src="https://picsum.photos/400/600" alt="avatar">
                  </v-avatar>
                </v-flex>
                <v-flex md4>
                  <v-card-text>
                      <p>Jean-Michel</p>
                      <p>Niveau</p>
                      <p>Ki</p>
                      <p>PV PM PA</p>
                  </v-card-text>
                </v-flex>
                <v-flex md4>
                  <v-card-text>
                    <p>Blabla</p>
                  </v-card-text>
                </v-flex>
              </v-layout>
            </v-container>
          </v-card>
        </v-flex>
        <v-flex d-flex md12>
          <v-tabs
              v-model="active"
              color="cyan"
              dark
              slider-color="yellow"
            >
              <v-tab
                v-for="n in 3"
                :key="n"
                ripple
              >
                Item {{ n }}
        
              </v-tab>
              <v-tab-item
                v-for="n in 3"
                :key="n"
              >
                <v-card color=red>
                  <v-card-text>{{ text }}</v-card-text>
                </v-card>
              </v-tab-item>
          </v-tabs>
        </v-flex>
      </v-layout>
        
    
    </v-container>
    <v-navigation-drawer
      temporary
      :right="right"
      v-model="rightDrawer"
      fixed
      app
    >
      <v-list>
        <v-list-tile @click="right = !right">
          <v-list-tile-action>
            <v-icon>compare_arrows</v-icon>
          </v-list-tile-action>
          <v-list-tile-title>Switch drawer (click me)</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-footer :fixed="fixed" app>
      <span>&copy; 2017</span>
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  components: {
    HelloWorld
  },
  data() {
    return {
      clipped: false,
      drawer: true,
      fixed: false,
      items: [
        {
          icon: "bubble_chart",
          title: "Inspire"
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Vuetify.js",
      active: null,
      text:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
    };
  }
};
</script>
