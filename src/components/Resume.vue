<template>
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
</template>

<script>
export default {
  name: "Resume",
  data() {
    return {
      postures: ["Défensive", "Offensive", "Attentive", "Charismatique"],
      text:
        "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corporis earum modi, mollitia necessitatibus vitae, voluptas dicta quia, neque voluptates eius ea velit dolor doloribus expedita. Excepturi hic delectus facere quas!"
    };
  }
};
</script>

