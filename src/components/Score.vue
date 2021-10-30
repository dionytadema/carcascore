<template>
  <v-tab-item class="pt-2">
    <div class="ma-2">
      Score
    </div>
    <v-expansion-panels inset>
      <v-subheader>Base Projects</v-subheader>
      <Road/>
      <City/>
      <Monastic/>
      <v-subheader>Cathedrals and Castles</v-subheader>
      <v-subheader>Expansions</v-subheader>
    </v-expansion-panels>
  </v-tab-item>
</template>

<script>
import Road from './score/Road.vue'
import City from './score/City.vue'
import Monastic from './score/Monastic.vue'

export default {
  name: 'score',
  components: {
    Road,
    City,
    Monastic,
  },
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
