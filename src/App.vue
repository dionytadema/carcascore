<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark>
      <div class="d-flex align-center">
        <v-img :src="require('@/assets/logo.png')"
          class="shrink mr-2" transition="scale-transition"
          alt="CarcasScore Logo"
          height="40" contain/>
      </div>
      <v-spacer></v-spacer>
      <v-btn @click="dark">
        <v-icon>mdi-brightness-3</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-tabs v-model="tab" 
        centered
        show-arrows>
        <v-tab>Parts</v-tab>
        <v-tab>Setup</v-tab>
        <v-tab>Draw Tile</v-tab>
        <v-tab>Tile</v-tab>
        <v-tab>Tile Actions</v-tab>
        <v-tab>Meeple</v-tab>
        <v-tab>Meeple Actions</v-tab>
        <v-tab>Score</v-tab>
        <v-tab>Score Actions</v-tab>
      </v-tabs>
      <v-tabs-items v-model="tab">
        <parts/>
        <setup/>
        <draw/>
        <draw/>
        <draw/>
        <draw/>
        <score/>
        <draw/>
      </v-tabs-items>
    </v-main>
  </v-app>
</template>

<script>
import Parts from './components/Parts';
import Setup from './components/Setup';
import Draw from './components/Draw';
import Score from './components/Score';

export default {
  name: 'App',
  components: {
    Parts,
    Setup,
    Draw,
    Score,
  },
  data: ()=>({
    tab: null,
  }),
  methods: {
    dark() {
      this.$vuetify.theme.dark = !this.$vuetify.theme.dark;
    },
  },
};
</script>

<style>
.theme--dark.v-tabs-items {
  padding-bottom: 25vh;
  background-color: #0000;
}
div.xlabel {
  position: absolute;
  bottom: 0px;
  right: 4px;
  color: black;
  font-weight: bold;
  text-shadow:
    0.15em 0rem 0.2em white,
    -0.15em 0rem 0.2em white,
    0rem 0.15em 0.2em white,
    0rem -0.15em 0.2em white;
}
</style>