<template>
  <div id="app">
    <main>
      <div class="search-box">
        <input type="text" class="search-bar" placeholder="Search ...">
        <div class="test" id="yes"></div>
      </div>

      <div class="weather-wrap">
        <div class="location-box">
          <div class="date">26 juillet 2022</div>
          <div class="location">Lyon, France</div>
        </div>

        <div class="weather-box">
          <div class="temp">9°C</div>
          <div class="weather">la pluie</div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>

import env from '@/env'

export default {
  name: 'App',
  components: {
    
  },
  data(){
    return {
      api_key: env.apikey
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
  font-family: 'monstserrat', sans-serif;
}

#app{
  background-image: url('./assets/cold-background.jpg');
  background-size: cover;
  background-position: bottom;
  transition: .4s;
}

main{
  min-height: 100vh;
  padding: 25px;
  background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0.25) rgba(0, 0, 0, 0.75));
}

.search-box{
  width: 100%;
  margin-bottom: 30px;

}

.search-box .search-bar{
  display: block;
  width: 100%;
  padding: 15px;
  color: #313131;
  font-size: 20px;

  appearance: none;
  border: none;
  outline: none;
  background: none;

  box-shadow: 0 0 8px rgba(0, 0, 0, 0.25);
  background-color: rgba(255, 255, 255, 0.15);
  border-radius: 0 16px 0 16px;

  transition: 1s;
}

.search-box .search-bar:focus {
  background-color: rgba(255, 255, 255, 0.75);
  box-shadow: 0 0 46px rgba(0, 0, 0, 0.25);
  border-radius: 16px 0 16px 0;
  color: red; 
}

.location-box .location {
  color: #fff;
  font-size: 32px;
  font-weight: 500;
  text-align: center;
  text-shadow: 4px 1px rgba(0, 0, 0, 0.9);
}

.location-box .date{
  color: #fff;
  font-size: 20px;
  font-weight: 300;
  font-style: italic;
  text-align: center;
}

.weather-box{
  text-align: center;
}

.weather-box .temp{
  display: inline-block;
  padding: 10px 25px;
  color: #fff;
  font-size: 102px;
  font-weight: 900;
  text-shadow: 3px 6px rgba(0, 0, 0, 0.7);
  background-color: rgba(255, 255, 255, 0.25);
  border-radius: 16px;
  margin: 30px 0;
  box-shadow: 3px 6px rgba(0, 0, 0, 0.5);
}

.weather-box .weather{
  color: #fff;
  font-size: 48px;
  font-weight: 700;
  font-style: italic;
  text-shadow: 3px 6px rgba(0, 0, 0, 0.25);
}

</style>
