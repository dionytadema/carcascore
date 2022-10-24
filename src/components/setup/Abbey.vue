<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require('@/assets/Abbey/Tile_01.jpg')"
        class="shrink mr-2" transition="scale-transition"
        width="40" contain/>
      Abbeys
      <v-img :src="require('@/assets/Abbey/Symbol_light.png')"
        class="shrink mx-2" transition="scale-transition"
        width="40" contain/>
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      Give every player one or more abbies
      <v-simple-table dense>
        <template v-slot:default>
          <thead>
            <tr><th>Players</th>
              <th v-for="h, i in header" :key="i">{{h}}</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="t, i in tiles" :key="i">
              <td>{{i}}</td>
              <td>{{t[0]}}</td>
              <td>{{t[1]}}</td>
              <td>{{t[2]}}</td>
            </tr>
          </tbody>
        </template>
      </v-simple-table>
      During the game a player may chose to use an abbey tile instead of drawing one from the regular stack, an abbey tile must be placed so it is orthogonally surrounded.
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'abbey',
  //components: {},
  //props: {},
  data: ()=>({
    header: ["up to 200","200 - 400","400+"],
    tiles: {
      2: [1, 2, 3],
      3: [1, 2, 2],
      4: [1, 1, 1],
      5: [1, 1, 1],
      6: [1, 1, 1],
    }
  }),
  //computed: {},
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
