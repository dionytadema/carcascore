<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require('@/assets/Halfling/Tile_A.png')"
        class="shrink mr-2" transition="scale-transition"
        width="40" contain/>
      Halflings
      <v-img :src="require('@/assets/Halfling/Symbol_light.png')"
        class="shrink mx-2" transition="scale-transition"
        width="40" contain/>
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      Distribute the half tiles evenly over all players
      <v-simple-table dense>
        <template v-slot:default>
          <thead>
            <tr><th>Players</th><th>Tiles</th></tr>
          </thead>
          <tbody>
            <tr v-for="t, i in tiles" :key="i">
              <td>{{i}}</td><td>{{t}}</td>
            </tr>
          </tbody>
        </template>
      </v-simple-table>
      During the game players can chose to use a half tile instead of drawing one from the regular stack
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'half',
  //components: {},
  //props: {},
  data: ()=>({
    tiles: {
      2: "3-12",
      3: "3-8",
      4: "3-6",
      5: "3-4",
      6: 3,
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
