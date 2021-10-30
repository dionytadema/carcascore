<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require(`@/assets/${game.path}/${icon}`)"
        width="40" class="shrink mr-2" transition="scale-transition">
        <div class="xlabel" v-if="total">{{total}}</div>
      </v-img>
      {{game.name}}<br>{{game.sub}}
    </v-expansion-panel-header>
    <v-expansion-panel-content class="pt-2">
      <v-subheader v-if="pieces.length">Pieces</v-subheader>
      <v-row>
        <v-col v-for="p, i in pieces" :key="i"
          class="d-flex child-flex"
          :cols="3" :md="2" :lg="1">
          <v-img :src="require(`@/assets/${game.path}/${p.image}`)" 
            contain max-height="80px">
            <div class="xlabel">{{p.amount}}</div>
          </v-img>
        </v-col>
      </v-row>
      <v-subheader v-if="meeples.length">Meeples</v-subheader>
      <v-img v-for="m, i in meeples" :key="i"
        :src="require(`@/assets/${game.path}/${m.image}`)"
        contain class="shrink mr-2" max-height="80px">
        <div class="xlabel">{{m.amount}}</div>
      </v-img>
      <v-subheader v-if="game.tiles">Tiles</v-subheader>
      <Tiles v-if="game.tiles" :path="game.path"
        :tiles="tiles"/>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
import Tiles from '@/components/parts/Tiles.vue'

export default {
  name: 'gameparts',
  components: {
    Tiles
  },
  props: {
    game: Object
  },
  //data: ()=>({}),
  computed: {
    pieces() {return this.game.pieces??[]},
    meeples() {return this.game.meeples??[]},
    tiles() {return this.game.tiles??false},
    total() {
      let t = this.game.tiles??[]
      return (t.total??t.unique)??0
    },
    icon() {
      return this.$vuetify.theme.dark?
        "Symbol_light.png":"Symbol_dark.png"
    },
  },
  //methods: {},
  //watch: {},
  //beforeCreate() {},
  //beforeMount() {},
  //beforeUpdate() {},
  //beforeDestroy() {},
  //created() {},
  //mounted() {},
  //updated() {},
  //destroyed() {},
  //activated() {},
  //deactivated() {},
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>