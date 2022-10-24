<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require(`@/assets/${icon('Tower')}`)"
        width="40" class="shrink mr-2" transition="scale-transition"/>
      Tower 1
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
  name: 'tower1',
  components: {
    Tileslot,
  },
  //props: {},
  data: ()=>({
    left: [
      {i:"River", t:"Lakes", n:7},
      {i:"Monastery", n:6},
      {i:"Base", n:72},
    ],
    right: [
      {i:"Cathedral", n:6},
      {i:"River", n:10},
      {i:"River2", n:9},
      {i:"River2", n:9},
      {i:"RiverAE", n:14},
      {i:"Inn", n:18},
      {i:"Trader", n:24},
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
