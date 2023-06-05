<template>
  <div>
   <div v-for="anime in data" :key="anime.mal_id">
    {{ anime.entry[0].title}}
    <img :src="anime.entry[0].images.jpg.image_url">
   </div>
  </div>
</template>

<script>
// @ is an alias to /src
import fetchData from '@/data/fetchData'
import { ref } from 'vue'


export default ({
  name: 'HomeView',
  components: {
  },
  setup(){
    const data = ref()
    fetchData('recommendations/anime')
    .then(response =>{
      data.value = response.data
      console.log(data.value)
    } )
    
    return {data}
  }
})
</script>
