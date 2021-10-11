<template>
  <v-row>
    <v-col v-for="t, i in names.slice(0, num)" :key="t"
      class="d-flex child-flex"
      :cols="3*size" :md="2" :lg="1">
      <v-img :src="require(`@/assets/${path}/Tile_${t}.${ext}`)">
        <div class="xlabel">{{amount[i]||1}}</div>
      </v-img>
    </v-col>
  </v-row>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'tiles',
  //components: {},
  props: {
    path: String,
    tiles: [Object, Boolean],
  },
  data: ()=>({
    names: 'ABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890',
  }),
  computed: {
    ext() {return this.tiles?this.tiles.ext??'jpg':''},
    num() {return this.tiles?this.tiles.unique??0:0},
    size() {return this.tiles?this.tiles.size??1:1},
    amount() {return this.tiles?this.tiles.amount??[]:[]}
  },
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
