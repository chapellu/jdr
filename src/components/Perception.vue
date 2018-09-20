<template>
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
</template>

<script>
export default {
  name: "Perception",
  data() {
    return {
      items: [
        {
          action: "15 min",
          headline: "Brunch this weekend?",
          title: "Ali Connors",
          subtitle:
            "I'll be in your neighborhood doing errands this weekend. Do you want to hang out?"
        },
        {
          action: "2 hr",
          headline: "Summer BBQ",
          title: "me, Scrott, Jennifer",
          subtitle: "Wish I could come, but I'm out of town this weekend."
        },
        {
          action: "6 hr",
          headline: "Oui oui",
          title: "Sandra Adams",
          subtitle: "Do you have Paris recommendations? Have you ever been?"
        },
        {
          action: "12 hr",
          headline: "Birthday gift",
          title: "Trevor Hansen",
          subtitle:
            "Have any ideas about what we should get Heidi for her birthday?"
        },
        {
          action: "18hr",
          headline: "Recipe to try",
          title: "Britta Holt",
          subtitle:
            "We should eat this: Grate, Squash, Corn, and tomatillo Tacos."
        }
      ]
    };
  }
};
</script>
