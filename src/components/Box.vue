<template>
  <v-tab-item class="pt-2">
    <v-expansion-panels>
      <Bigbox/>
      <Tower1/>
      <Tower2/>
      <Anni/>
    </v-expansion-panels>
  </v-tab-item>
</template>

<script>
import Bigbox from '@/components/box/Bigbox.vue'
import Tower1 from '@/components/box/Tower1.vue'
import Tower2 from '@/components/box/Tower2.vue'
import Anni from '@/components/box/Anni.vue'

export default {
  name: 'box',
  components: {
    Bigbox,
    Tower1,
    Tower2,
    Anni,
  },
  //props: {},
  //data: ()=>({}),
  //computed: {},
  //methods: {},
  //watch: {},
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .row {
    display: flex;
  }
</style>
