<template>
   <MyHeader appName="Weather Cast" dateOfReport="04-27-2024" myName="Jhansi Sreya Jagarapu"/>
   <ContainerBox :weatherdata="weatherdata.weatherReport" />
</template>

<script>

   import MyHeader from './components/MyHeader.vue'
   import ContainerBox from './components/ContainerBox.vue'

   export default{
      name: 'App',
      components:{
          MyHeader,
          ContainerBox
      },
      data(){
        return{
          weatherdata : []
        }
      },
      methods: {
            async fetchdata(){
            const res = await fetch('https://nodejs-server-pf4m.onrender.com/api');
            const data = await res.json()
            console.log(data)
            return data
        }
      },
      async created() {
          this.weatherdata = await this.fetchdata();
      }
}

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.container {
  font-family: 'Montserrat', sans-serif;
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

</style>