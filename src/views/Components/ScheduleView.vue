<template>
  <div class="bg-zinc-200">Schedule</div>

  <div class="grid gap-4 grid-cols-2 bg-zinc-200 pl-2 pt-1 pr-5">
        
    <div v-for="anime in data" .key="anime" mal.id >
        
        <div class="flex bg-white p-2 m-2 rounded-l-2xl h-64 w-full">
            <img :src="anime.images.jpg.image_url" class="h-60 w-60 rounded-l-2xl bg-center">
            <div class="text-base text-left pl-2 pr-2">
                {{ anime.title }}<br><br>
                {{ anime.status }}
            </div>
           
        </div>

        
    </div>
  </div>
</template>

<script>
import fetchData from '@/data/fetchData'
import { ref } from 'vue'
export default ({
    setup(){
    const data = ref()
    fetchData('schedules')
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