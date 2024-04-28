<template>
   <div class="headerdata" v-for="wdata of weatherdata" 
   :key="wdata.id">
        <SingleCountry :wdata = wdata />
    </div>
</template>

<script>
import SingleCountry from './SingleCountry.vue'

export default{
  name: 'ContainerBox',
  props:{
    weatherdata: Array
  },
  components:{
    SingleCountry
  }
}
</script>

<style scoped>

</style>