<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img
        class="shrink mr-2"
        contain
        :src="require('@/assets/City/Tile_A.jpg')"
        width="40"/>
      De Stad Carcasonne
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      <ul>
        <li>Beide helften worden door een speler op een passende plaats aangelegt</li>
        <li>De active speler zet de graaf op een district naar keuze</li>
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
