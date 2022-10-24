<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require('@/assets/River/Tile_01.jpg')"
        class="shrink mr-2" transition="scale-transition"
        width="40" contain/>
      The Rivers
      <v-img :src="require('@/assets/River/Symbol_light.png')"
        class="shrink mx-2" transition="scale-transition"
        width="40" contain/>
      <v-img :src="require('@/assets/River2/Symbol_light.png')"
        class="shrink mr-2" transition="scale-transition"
        width="40" contain/>
      <v-img :src="require('@/assets/RiverAE/Symbol_light.png')"
        class="shrink mr-2" transition="scale-transition"
        width="40" contain/>
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      Pick on of the sources, then shake the lakes and river tiles separately and put all river tiles on top of the lakes. During the game players will first draw from the river stack untill the river is complete.
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'river',
  //components: {},
  //props: {},
  //data: ()=>({}),
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
