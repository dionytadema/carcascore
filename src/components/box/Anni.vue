<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require(`@/assets/${icon('Anniversary')}`)"
        width="40" class="shrink mr-2" transition="scale-transition"/>
      Aniversary Edition
    </v-expansion-panel-header>
    <v-expansion-panel-content class="pt-2">
      <div class="anivers">
        <div class="row">
          <Tileslot :list="top"/>
        </div>
        <div class="row">
          <Tileslot :list="mid_l"/>
          <Tileslot :list="mid_r"/>
        </div>
        <div class="row" style="flex:3">
          <div v-for="s, i in list" :key="i"
            class="slot">
            <div class="stack" :style="{flexGrow: Math.max(s.n-6,0)}">
              <v-img :src="require(`@/assets/${icon(s.i)}`)"
                contain max-width="32px">
                <div class="xlabel">{{s.n}}</div>
              </v-img>
              <span>{{s.t}}</span>
            </div>
          </div>
        </div>
      </div>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
import Tileslot from '@/components/parts/Tileslot.vue'

export default {
  name: 'anni',
  components: {
    Tileslot,
  },
  //props: {},
  data: ()=>({
    list: [
      {i:"Anniversary", n:72},
      {i:"Wheel", n:72},
    ],
    mid_l: [
      {i:"Abbey", n:18},
      {i:"Bridge", n:12},
    ],
    mid_r: [
      {i:"Gifts"},
      {i:"Bridge"},
    ],
    top: [
      {i:"Bridge"},
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
  .anivers {
    display: flex;
    flex-flow: column;
    height: 400px;
    max-width: 400px;
    margin: auto;
  }
</style>
