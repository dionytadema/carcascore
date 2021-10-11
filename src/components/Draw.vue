<template>
  <v-tab-item class="pt-2">
    <div class="ma-2">
      Eerst kiest men wat voor tegel deze beurt gelegt gaat worden, als met de rivier gespeelt word dan moet eerst de rivier afgebouwt worden
    </div>
    <v-expansion-panels inset>
      <v-subheader>The River</v-subheader>
      <river/>
      <v-subheader>Regular & Variant Tiles</v-subheader>
      <half/>
      <abbey/>
      <castle/>
      <v-subheader>Expanstions</v-subheader>
      <city/>
      <wheel/>
    </v-expansion-panels>
  </v-tab-item>
</template>

<script>
import River from './draw/River.vue'
import Half from './draw/Half.vue'
import Abbey from './draw/Abbey.vue'
import Castle from './draw/Castle.vue'
import City from './draw/City.vue'
import Wheel from './draw/Wheel.vue'

export default {
  name: 'draw',
  components: {
    River,
    Half,
    Abbey,
    Castle,
    City,
    Wheel,
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
