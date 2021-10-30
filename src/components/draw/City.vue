<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img
        class="shrink mr-2"
        contain
        :src="require('@/assets/City/Tile_A.jpg')"
        width="40"/>
      The city of Carcasonne
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      <ul>
        <li>The city of Carcassone is placed so its features connect.</li>
        <li>The active player places the count on the city hall</li>
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
