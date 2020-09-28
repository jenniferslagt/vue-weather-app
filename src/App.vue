<template>
  <div id="app" v-bind:class="typeof weather.main != 'undefined' && weather.main.temp > 17 ? 'warm' : ''">
    <main>
     <SearchBox @search="fetchWeather($event)" />
      <div class="weather-wrap" v-if="typeof weather.main != 'undefined'">
        <LocationBox v-bind:weather="weather"/>
        <WeatherBox v-bind:weather="weather"/>
      </div>
    </main>
  </div>
</template>

<script>
import SearchBox from "./components/SearchForm";
import LocationBox from "./components/LocationBox";
import WeatherBox from "./components/WeatherBox";

export default {
  name: 'App',
  components: {
    SearchBox,
    LocationBox,
    WeatherBox
  },
  data () {
    return {
      api_key: '327256d3ecc9391886aea340632ab22f',
      url_base: 'https://api.openweathermap.org/data/2.5/',
      weather: {} 
    }
  },
  methods: {
    fetchWeather(query) {   
        fetch(`${this.url_base}weather?q=${query}&units=metric&APPID=${this.api_key}`)
        .then(res => {
          return res.json();
        }).then(this.setResults)
    },
    setResults (results) {
      this.weather = results; 
    }
  }
}
</script>

<style>
 * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
 } 

 body {
   font-family: 'montserrat', sans-serif;
 }

 #app {
   background-image: url('https://images.unsplash.com/photo-1482160310982-3adf8b38daef?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80');
   background-size: cover;
   background-position: bottom;
   transition: 0.4s; 
 }

  #app.warm {
    background-image: url('https://images.unsplash.com/photo-1511860810434-a92f84c6f01e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80');
  }

  main {
    min-height: 100vh;
    padding: 25px;
    background: rgb(2,0,36);
    background: linear-gradient(0deg, rgba(2,0,36,0.2) 0%, rgba(4,4,56,0.2) 35%); 
  }
</style>
