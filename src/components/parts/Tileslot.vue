<template>
  <div class="slot">
    <div v-for="s, i in list" :key="i"
      class="stack" :style="{flexGrow: Math.max(s.n-6,0)}">
      <v-img :src="require(`@/assets/${icon(s.i)}`)"
        contain max-width="36px">
        <div class="xlabel">{{s.n}}</div>
      </v-img>
      <span v-if="s.t">{{s.t}}</span>
    </div>
  </div>
</template>

<script>
//import Empty from './Empty.vue'

export default {
  name: 'tileslot',
  //components: {},
  props: {
    list: Array,
  },
  //data: ()=>({}),
  //computed: {},
  methods: {
    icon(exp) {
      return `${exp}/Symbol_${this.$vuetify.theme.dark?"light":"dark"}.png`
    },
  },
  //watch: {},
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .slot {
    flex: 3;
    display: flex;
    flex-flow: column;
    margin: 4px;
    padding: 6px;
    border-radius: 12px;
    border: 2px #8888 solid;
  }
  .slot.small {
    flex: 1;
    margin: 32px 4px; 
    padding: 6px 6px;
    border-radius: 24px;
    display: flex;
    justify-content: center;
  }
  .stack {
    display: flex;
    align-items: center;
    padding: 8px;
    border: 1px #888 solid;
  }
  .stack span {
    padding-left: 12px;
  }
</style>
