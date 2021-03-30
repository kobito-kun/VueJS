<template>
  <Information v-if="openInformation" :object="openInformationObject" @close-emit="closeInfo" />
  <Hero />
  <div class="grid lg:grid-cols-4 md:grid-cols-3 grid-cols-2 bg-gray-100">
    <Item @this-data="data" v-for="item in results" :key="item.id" :data="item" />
  </div>
</template>

<script>
import Hero from "./components/Hero.vue";
import Item from "./components/Item.vue";
import Information from "./components/Information.vue";
import axios from 'axios';

export default {
  name: 'App',
  components: {
    Hero,
    Item,
    Information,
  },
  data(){
    return {
      results: null,
      openInformation: false,
      openInformationObject: null,
    }
  },
  mounted(){
      axios.get("https://api.punkapi.com/v2/beers").then(response => (this.results = response.data)).then(response => console.log(response))
  },
  methods: {
    data(data){
      this.openInformation = !this.openInformation
      this.openInformationObject = data
      console.log(this.openInformationObject)
    },
    closeInfo(){
      this.openInformation = !this.openInformation
    }
  },
}
</script>

<style>
@import './assets/all.css';
</style>
