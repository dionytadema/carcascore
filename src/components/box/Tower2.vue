<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require(`@/assets/${icon('Tower')}`)"
        width="40" class="shrink mr-2" transition="scale-transition"/>
      Tower 2
    </v-expansion-panel-header>
    <v-expansion-panel-content class="pt-2">
      <div class="tower">
        <Tileslot :list="left"/>
        <Tileslot :list="right"/>
      </div>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
import Tileslot from '@/components/parts/Tileslot.vue'

export default {
  name: 'tower2',
  components: {
    Tileslot,
  },
  //props: {},
  data: ()=>({
    left: [
      {i:"Base", t:"Point tiles", n:4},
      {i:"Abbey", t:"Abbeys", n:6},
      {i:"Dragon", n:30},
      {i:"Tower", n:18},
      {i:"Abbey", n:12},
      {i:"City", n:10},
      {i:"Bridge", n:12},
    ],
    right: [
      {i:"Labyrinth", n:2},
      {i:"Hill", n:18},
      {i:"Circus", n:18},
      {i:"Arrows", n:15},
      {i:"Crop", n:6},
      {i:"Tree", n:6},
      {i:"Peasant", n:12},
      {i:"Watchtower", n:12},
    ],
  }),
  //computed: {},
  methods: {
    icon(exp) {
      return `${exp}/Symbol_${this.$vuetify.theme.dark?"light":"dark"}.png`
    },
  },
  //watch: {},
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .tower {
    display: flex;
    height: 600px;
    max-width: 400px;
    margin: auto;
  }
</style>
