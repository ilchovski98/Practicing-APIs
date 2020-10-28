<template>
  <div id="app">
    <Header></Header>

    <HeaderSecondary>
      <fetcher class="space" :url="url1">
        <template #default="{ apiData }">
          <span>{{ apiData.current_price }}</span>
        </template>
      </fetcher>
    </HeaderSecondary>

    <fetcher class="space" :url="url1">
      <template #default="{ apiData }">
        <card>
          <template v-slot:card__name>
            {{ apiData.name }}
          </template>

          <template v-slot:card__price>
            {{ apiData.current_price }} $
          </template>
        </card>
      </template>
    </fetcher>
  </div>
</template>

<script>
import Card from './components/card'
import Header from './components/header'
import HeaderSecondary from './components/header-secondary'
import Fetcher from './components/fetcher'
// import StockPreview from './components/stock-preview'
import "bootstrap/dist/css/bootstrap.min.css"

export default {
  name: 'App',
  components: {
    Card,
    Fetcher,
    Header,
    HeaderSecondary,
    // StockPreview
  },
  data() {
    return {
      url1: 'https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=100&page=1&sparkline=false',
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
}
</style>
