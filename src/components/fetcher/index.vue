<template>
  <div>
      <slot :apiData="apiData"></slot>
  </div>
</template>

<script>
import axios from "axios"
export default {
    name: 'Fetcher',
    props: ['url'],
    data() {
        return {
            apiData: ''
        }
    },
    mounted() {
        axios.get(this.url).then(response => {
            this.apiData = response.data
        })
    }
}
</script>

<style>

</style>