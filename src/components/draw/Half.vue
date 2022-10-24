<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img
        class="shrink mr-2"
        contain
        :src="require('@/assets/Halfling/Tile_01.png')"
        transition="scale-transition"
        width="40"/>
      Halfling
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      <ul>
        <li>Een halve tegel moet met 1 zijde aansluiten</li>
        <li>Op een halve tegel mag alleen een brug gebouwt worden als deze een andere halve tegel compleet maakt</li>
      </ul>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'half',
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
