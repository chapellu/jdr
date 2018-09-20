<template>
    <v-tabs v-model="active" color="cyan" dark slider-color="yellow" lg9 grow>
        <v-tab v-for="tab in tabs" ripple :key=tab>
            {{tab.title}}
        </v-tab>
        <v-tab-item v-for="tab in tabs" :key=tab>
            <v-card color=red>
              <v-card-text v-bind:is="tab.contents"></v-card-text>
            </v-card>
        </v-tab-item>
    </v-tabs>
</template>

<script>
import Statistiques from "./Statistiques";
export default {
  name: "Menu",
  components: {
    Statistiques
  },
  data() {
    return {
      tabs: [
        { title: "Statistiques", contents: "Statistiques" },
        { title: "Inventaire", contents: "text" },
        { title: "Craft", contents: "text" },
        { title: "Tableaux", contents: "text" },
        { title: "Journal", contents: "text"}
      ]
    };
  }
};
</script>

