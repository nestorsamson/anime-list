<template>
    <div class="bg-zinc-200 h-64 ">
        <div class="flex pl-2">Recommendations</div>
        <div class="flex overflow-auto overflow-y-hidden">

            <div v-for="anime in data" :key="anime.mal_id">
                <RecomendationCards :anime="anime"/>
            </div> 

        </div>
  </div>
</template>

<script>
import fetchData from '@/data/fetchData'
import { ref } from 'vue'
import RecomendationCards from './RecomendationCards.vue'
export default ({
    components: {
        RecomendationCards
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

<style>

</style>