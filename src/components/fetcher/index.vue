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
            apiData: '',
            timer: ''
        }
    },
    created () {
        this.fetchEventsList();
        this.timer = setInterval(this.fetchEventsList, 70000)
    },
    methods: {
        fetchEventsList() {
            axios.get(this.url).then(response => {
                this.apiData = response.data[0];
                console.log(response.data[0]);
            })
        }
    }
}
</script>

<style>

</style>