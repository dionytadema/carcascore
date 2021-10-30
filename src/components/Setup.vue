<template>
  <v-tab-item class="pt-2">
    <div class="ma-2">
      <v-subheader>Pick Expansions</v-subheader>
      Pick which expansions you want to play and execute the steps below for each of them
    </div>
    <v-expansion-panels inset>
      <River/>

      <Abbey/>
      <Half/>
    </v-expansion-panels>
  </v-tab-item>
</template>

<script>
import River from './setup/River.vue'
import Half from './setup/Half.vue'
import Abbey from './setup/Abbey.vue'
//import Castle from './setup/Castle.vue'

export default {
  name: 'setup',
  components: {
    River,
    Half,
    Abbey,
    //Castle,
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
