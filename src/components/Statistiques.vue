<template>
    <div>
        <v-flex lg12>
            <v-card color="primary">
                <v-card-title>Famille</v-card-title>
                <v-flex lg12 d-flex column>
                    <v-flex lg8>
                        <v-card-text>
                            <p>Nom</p>
                            <p>Niveau</p>
                        </v-card-text>
                    </v-flex>
                    <v-flex lg4>
                        <Statistic :stats=stats substats=""></Statistic>
                    </v-flex>
                </v-flex>
            </v-card>   
        </v-flex>
        <v-flex lg12>
            <v-card color="primary">
                <v-card-title>Corps</v-card-title>
                <v-flex lg12 d-flex column>
                    <v-flex lg8>
                        <v-card-text>
                            <p>Nom</p>
                            <p>Niveau</p>
                        </v-card-text>
                    </v-flex>
                    <v-flex lg4>
                        <Statistic :stats=stats substats=""></Statistic>
                    </v-flex>
                </v-flex>
            </v-card>   
        </v-flex>
        <v-flex lg12>
            <v-card color="primary">
                <v-card-title>Esprit</v-card-title>
                <v-flex lg12 d-flex column>
                    <v-flex lg8>
                        <v-card-text>
                            <p>Nom</p>
                            <p>Niveau</p>
                        </v-card-text>
                    </v-flex>
                    <v-flex lg4>
                        <Statistic :stats=stats substats=""></Statistic>
                    </v-flex>
                </v-flex>
            </v-card>   
        </v-flex>
    </div>
</template>

<script>
import Statistic from "./Statistic";
export default {
  name: "Statistiques",
  components: { Statistic },
  data() {
      return {
          stats: {title: "Testy", values: {base: 64}}
      };
  }
};
</script>
