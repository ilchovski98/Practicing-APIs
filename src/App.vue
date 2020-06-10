<template>
  <div id="app">
    
    <fetcher class="space" :url="url1">
      <template #default="{ apiData }">
        <card>{{ apiData.name }}</card>
      </template>
    </fetcher>

    <fetcher class="space" :url="url2">
      <template #default="{ apiData }">
        <card>{{ apiData.name }}</card>
      </template>
    </fetcher>

    <fetcher class="space" :url="url3">
      <template #default="{ apiData }">
        <card>{{ apiData.name }}</card>
      </template>
    </fetcher>

    <fetcher class="space" :url="url4">
      <template #default="{ apiData }">
        <card>{{ apiData.name }}</card>
      </template>
    </fetcher>
  </div>
</template>

<script>
import Card from './components/card'
import Fetcher from './components/fetcher'
import "bootstrap/dist/css/bootstrap.min.css"


export default {
  name: 'App',
  components: {
    Card,
    Fetcher
  },
  data() {
    return {
      url1: 'https://swapi.dev/api/planets/1/',
      url2: 'https://swapi.dev/api/planets/2/',
      url3: 'https://swapi.dev/api/planets/3/',
      url4: 'https://swapi.dev/api/planets/4/'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-wrap: wrap;
}

.space {
  margin: 20px;
}
</style>
