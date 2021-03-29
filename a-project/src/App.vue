<template>
  <Hero />
  <div class="grid grid-cols-4 bg-gray-100">
    <Item v-for="item in results" :key="item.id" :data="item" />
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Item from "./components/Item.vue";
import axios from 'axios';

export default {
  name: 'App',
  components: {
    Hero,
    Item,
  },
  data(){
    return {
      results: null
    }
  },
  mounted(){
      axios.get("https://api.punkapi.com/v2/beers").then(response => (this.results = response.data)).then(response => console.log(response))
  },
}
</script>

<style>
@import './assets/all.css';
</style>
