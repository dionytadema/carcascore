<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require('@/assets/Base/Tile_01.jpg')"
        class="shrink mr-2" transition="scale-transition"
        width="40" contain/>
      Monastery
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      A monastery consists of it's tile and the 8 surrounding tiles
      <ul>
        <li>1 points per tile</li>
        <li>+3 points per vineyard</li>
        <li>+3 points if the fairy is on the monastery</li>
        <li>+1 points per tile when a the mage is on the monastery</li>
      </ul>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'monastic',
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
