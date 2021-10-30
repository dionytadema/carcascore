<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require(`@/assets/${icon('Base')}`)"
        width="40" class="shrink mr-2" transition="scale-transition">
      </v-img>
      Big Box
    </v-expansion-panel-header>
    <v-expansion-panel-content class="pt-2">
      <div class="bigbox">
        <div class="row">
          <div v-for="s, i in top" :key="i"
            class="slot">
            <div class="stack" :style="{flexGrow: Math.max(s.n-6,0)}">
              <v-img :src="require(`@/assets/${icon(s.i)}`)"
                contain max-width="32px">
                <div class="xlabel">{{s.n}}</div>
              </v-img>
              <v-img v-if="i==1" :src="require(`@/assets/${icon('School')}`)"
                contain max-width="32px">
                <div class="xlabel">2</div>
              </v-img>
            </div>
          </div>
        </div>
        <div class="row">
          <Tileslot :list="mid_l"/>
          <div class="slot small">
            <div v-for="s, i in mid_m" :key="i"
              class="stack" :style="{flexGrow: Math.max(s.n-6,0)}">
              <v-img :src="require(`@/assets/${icon(s.i)}`)"
                contain max-width="32px">
                <div class="xlabel">{{s.n}}</div>
              </v-img>
              <span>{{s.t}}</span>
            </div>
          </div>
          <Tileslot :list="mid_r"/>
        </div>
        <div class="row">
          <Tileslot :list="bot_l"/>
          <Tileslot :list="bot_m"/>
          <Tileslot :list="bot_r"/>
        </div>
      </div>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
import Tileslot from '@/components/parts/Tileslot.vue'

export default {
  name: 'box',
  components: {
    Tileslot,
  },
  //props: {},
  data: ()=>({
    top: [
      {i:"Inn", n:18},
      {i:"Halfling", n:24},
      {i:"Trader", n:24},
    ],
    mid_l: [
      {i:"Bathhouse", n:6},
      {i:"Festival", n:10},
    ],
    mid_m: [
      {i:"Hill"},
    ],
    mid_r: [
      {i:"River", t:"Sources", n:3},
      {i:"Tollkeeper", n:10},
      {i:"City", n:10},
      {i:"Tower", n:18},
    ],
    bot_l: [
      {i:"Flier", n:8},
      {i:"Goldmine", n:8},
    ],
    bot_m: [
      {i:"Message", n:8},
      {i:"Mage", n:8},
    ],
    bot_r: [
      {i:"Ferrie", n:8},
      {i:"Robber", n:8},
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
  .bigbox {
    display: flex;
    flex-flow: column;
    max-width: 400px;
    margin: auto;
  }
</style>
