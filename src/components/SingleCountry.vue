<template>
  <div
    class="singlebox"
    :class="{
      'orange': wdata.weatherDescription === 'Sunny',
      'blue': wdata.weatherDescription === 'Rainy',
      'gray': wdata.weatherDescription === 'Cloudy',
      'cyan': wdata.weatherDescription === 'Snowy'
    }"
  >
    <h2 class="locationName">{{ wdata.locationName }}</h2>
    <img class="weather-image" :src="wdata.urlimage" alt="Weather Image" />
    <h4 class="allh4">Temperatue: {{ wdata.temperature }}&deg;C</h4>
    <h4 class="allh4">Humidity: {{ wdata.humidity }}%</h4>
    <h4 class="allh4">WindSpeed: {{ wdata.windSpeed }} km/hr</h4>
    <h4 class="allh4">WeatherDescription: {{ wdata.weatherDescription }}</h4>
    <h4 class="allh4">Sunrise Time: {{ wdata.sunriseTime }}</h4>
    <h4 class="allh4">Sunset Time: {{ wdata.sunsetTime }}</h4>
    <h4 class="allh4">UV Index: {{ wdata.uvIndex }}</h4>
  </div>
</template>

<script>
export default {
  name: 'SingleCountry',
  props: {
    wdata: Array
  },
}
</script>

<style scoped>
.allh4 {
  margin: 5px;
}

.singlebox {
  background-color: #ffb89e;
  color: black;
  padding: 10px;
  text-align: center;
  width: 50%;
  margin: auto;
  font-family: 'Montserrat', sans-serif;
  margin-bottom: 20px;
}
.weather-image {
  max-width: 60px;
  max-height: 60px;
  margin-bottom: 20px;
}
.orange {
  background-color: lightcoral;
}
.blue {
  background-color: lightblue;
}
.cyan {
  background-color: cyan;
}
.gray {
  background-color: lightgray;
}
</style>