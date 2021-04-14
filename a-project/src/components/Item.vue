<template>
<div class="p-10">  
  <div style="min-width: 250px; min-height: 430px;" @click="openInformation" class="max-w-sm rounded overflow-hidden shadow-lg cursor-pointer transform hover:scale-105 duration-150 bg-white border-blue-500 border-l-4">
    <img class="image mx-auto block" :src="data.image_url" :alt="data.name">
    <div class="px-6 py-4">
      <div class="font-bold text-sm mb-2">{{data.name}}</div>
      <p class="text-gray-700 text-base">
        {{data.description.slice(0,85) }}...
      </p>
    </div>
    <div class="px-6 pt-4 pb-2">
      <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">{{data.first_brewed}}</span>
    </div>
  </div>
</div>
</template>

<script>
export default {
    name: 'Item',
    props: {
        data : Object,
    },
    methods: {
      openInformation(){
        console.log(this.data.id)
        this.$emit('this-data', this.data)
      }
    },
}
</script>

<style>
.image{
    max-width: 150px;
    max-height: 200px;
}
</style>