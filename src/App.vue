<template>
  <v-app>
    <v-container fluid grid-list-md>
      <v-layout row wrap>
        <v-flex d-flex lg12>
          <v-card color=purple dark>
            <v-container fluid grid-list-md>
              <v-layout row align-center justify-center align-content-space-around>
                <v-flex md3 >
                  <v-avatar tile size=200>
                    <img src="https://picsum.photos/400/600" alt="avatar">
                  </v-avatar>
                </v-flex>
                <v-flex md3>
                  <v-card-text>
                      <p>Jean-Michel</p>
                      <p>Niveau</p>
                      <p>Ki</p>
                      <p>PV PM PA</p>
                  </v-card-text>
                </v-flex>
                <v-flex md2 mr-4>
                  <v-select
                    :items="postures"
                    label="Posture"
                    append-icon="info"
                  ></v-select>
                </v-flex>
                <v-flex md4>
                  <v-textarea disabled :value=text></v-textarea>
                </v-flex>
              </v-layout>
            </v-container>
          </v-card>
        </v-flex>
          <v-flex d-flex lg9>
            <v-tabs
                v-model="active"
                color="cyan"
                dark
                slider-color="yellow"
                lg9
                grow
              >
                <v-tab
                  v-for="tab in tabs"
                  ripple
                  :key=tab
                >
                  {{tab}}
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
          <v-flex lg3>
            <v-card color=blue>
              <v-toolbar color=blue dark>
                <v-toolbar-title>Perception</v-toolbar-title> 
              </v-toolbar>
              <v-list two-line>
                <template v-for="(item, index) in items">
                  <v-list-tile :key="index" avatar ripple @click="">
                    <v-list-tile-content>
                      <v-list-tile-title>{{ item.title }}</v-list-tile-title>
                      <v-list-tile-sub-title class="text--primary">{{ item.headline }}</v-list-tile-sub-title>
                      <v-list-tile-sub-title>{{ item.subtitle }}</v-list-tile-sub-title>
                    </v-list-tile-content>
                  </v-list-tile>
                  <v-divider v-if="index + 1 < items.length" :key="`divider-${index}`"></v-divider>
                </template>
              </v-list>
            </v-card>
          </v-flex>
        <v-flex>
          <v-card lg12 color=yellow>Techniques</v-card>
        </v-flex>
      </v-layout>
    </v-container>
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
      postures: ["Défensive", "Offensive", "Attentive", "Charismatique"],
      tabs: ["Statistiques", "Inventaire", "Craft", "Tableaux"],
      items: [
        { action: '15 min', headline: 'Brunch this weekend?', title: 'Ali Connors', subtitle: "I'll be in your neighborhood doing errands this weekend. Do you want to hang out?" },
        { action: '2 hr', headline: 'Summer BBQ', title: 'me, Scrott, Jennifer', subtitle: "Wish I could come, but I'm out of town this weekend." },
        { action: '6 hr', headline: 'Oui oui', title: 'Sandra Adams', subtitle: 'Do you have Paris recommendations? Have you ever been?' },
        { action: '12 hr', headline: 'Birthday gift', title: 'Trevor Hansen', subtitle: 'Have any ideas about what we should get Heidi for her birthday?' },
        { action: '18hr', headline: 'Recipe to try', title: 'Britta Holt', subtitle: 'We should eat this: Grate, Squash, Corn, and tomatillo Tacos.' }
      ],
      text:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
    };
  }
};
</script>
