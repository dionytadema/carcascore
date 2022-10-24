<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img :src="require('@/assets/Base/Tile_03.jpg')"
        class="shrink mr-2" transition="scale-transition"
        width="40" contain/>
      City
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      <ul>
        <li>2 points per tile</li>
        <li>2 points per weapon</li>
        <li>3 points per castle that exists within the cities tiles</li>
        <li>+1 points per tile when a cathedral is in the city</li>
        <li>+1 points per tile when a the mage is in the city</li>
      </ul>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'city',
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
