<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require('@/assets/Base/Tile_U.jpg')"
        class="shrink mr-2" transition="scale-transition"
        width="40" contain/>
      Road
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      <ul>
        <li>1 points per tile</li>
        <li>+1 points per tile when a inn is next to the road</li>
        <li>+1 points per tile when a the mage is on the road</li>
      </ul>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'road',
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
