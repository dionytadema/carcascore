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
          <div class="slot"/>
          <div class="slot"/>
        </div>
        <div class="row">
          <div class="slot"/>
          <div class="slot"/>
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

export default {
  name: 'anni',
  //components: {},
  //props: {},
  data: ()=>({
    list: [
      {i:"Anniversary", n:72},
      {i:"Wheel", n:72},
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
