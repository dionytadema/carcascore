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
        <v-tab key="0">Parts</v-tab>
        <v-tab key="1">Box</v-tab>
        <v-tab key="2">Setup</v-tab>
        <v-tab key="3">Tile</v-tab>
        <v-tab key="4">Meeple</v-tab>
        <v-tab key="5">Score</v-tab>
        <v-tab key="6">Action</v-tab>
      </v-tabs>
      <v-tabs-items v-model="tab">
        <Parts key="0"/>
        <Box key="1"/>
        <Setup key="2"/>
        <Draw key="3"/>
        <Draw key="4"/>
        <Score key="5"/>
        <Score key="6"/>
      </v-tabs-items>
    </v-main>
  </v-app>
</template>

<script>
import Parts from './components/Parts';
import Box from './components/Box';
import Setup from './components/Setup';
import Draw from './components/Draw';
import Score from './components/Score';

export default {
  name: 'App',
  components: {
    Parts,
    Box,
    Setup,
    Draw,
    Score,
    //Actions,
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