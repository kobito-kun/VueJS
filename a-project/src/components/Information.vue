<template>
<div id="div" class="h-screen w-screen">
  <div class="flex items-center justify-center h-screen">
    <button class="py-2 px-4 bg-red-400" style="position: fixed; top: 10px; left: 10px;" @click="closeOpenInformation">Close</button>
      <div class="grid lg:grid-cols-2 mx-20 lg:mx-80">
          <div>
            <img :src="object.image_url" class="w-20 block mx-auto" />
            <h3 class="font-bold text-2xl text-center">{{object.name}}</h3>
          </div>
          <div class="bg-black text-white rounded shadow p-5">
            <p><span class="font-bold">Tagline</span>: {{object.tagline}}</p>
            <p><span class="font-bold">First brewed</span>: {{object.first_brewed}}</p>
            <p><span class="font-bold">Description</span>: {{object.description}}</p>
            <p><span class="font-bold">Pairings</span>: 
              <ul v-for="item in object.food_pairing" :key="item" >
                <li>{{item}}</li>
              </ul>
            </p>
            <p><span class="font-bold text">Volume</span>: {{object.volume.value}}</p>
          </div>
      </div>
  </div>
</div>
</template>

<script>
export default {
    name: 'Information',
    props: {
        object: Object,
    },
    methods: {
      closeOpenInformation(){
          this.$emit("close-emit", false)
      }  
    },
}
</script>

<style scoped>
#div{
    position: fixed;
    z-index: 1000;
    background: rgba( 255, 255, 255, 0.25 );
    box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
    backdrop-filter: blur( 9.0px );
    -webkit-backdrop-filter: blur( 9.0px );
    border-radius: 10px;
    border: 1px solid rgba( 255, 255, 255, 0.18 );    
}
</style>