<template>
  <v-row>
    <v-col v-for="i in num" :key="i"
      class="d-flex child-flex"
      :cols="size(i)" :md="2" :lg="1">
      <v-img :src="require(`@/assets/${path}/Tile_${pad(i)}.${ext}`)">
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
  data: ()=>({}),
  computed: {
    ext() {return this.tiles?.ext??'jpg'},
    num() {return this.tiles?.unique??0},
    amount() {return this.tiles?.amount??[]}
  },
  methods: {
    pad(n) {
      let num = n.toString()
      if (num.length < 2) return "0" + num
      return num
    },
    size(i) {return 3 * ( (this.tiles?.size?.[i]??this.tiles?.size)-0 || 1)},
  },
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
