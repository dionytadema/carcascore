<template>
  <v-expansion-panel>
    <v-expansion-panel-header>
      <v-img
        alt="Kasteel"
        class="shrink mr-2"
        contain
        :src="require('@/assets/Market/Tile_A.jpg')"
        transition="scale-transition"
        width="40"/>
      Duits Kasteel
    </v-expansion-panel-header>
    <v-expansion-panel-content>
      <ul>
        <li>Een kasteel mag geen andere kastelen hebben op omringende tegels</li>
      </ul>
    </v-expansion-panel-content>
  </v-expansion-panel>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'castle',
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
