<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img
        class="shrink mr-2"
        contain
        :src="require('@/assets/Abbey/Tile_A.jpg')"
        transition="scale-transition"
        width="40"/>
      Abdij
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      <ul>
        <li>Een abdij moet aan alle zijdes omringt zijn</li>
        <li>Op een abdij mag alleen een monik gezet worden</li>
      </ul>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'abbey',
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
