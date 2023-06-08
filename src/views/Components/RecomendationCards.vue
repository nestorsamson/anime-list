<template>
    <div class="relative p-2 m-2 rounded-2xl h-46 w-40 ">
            <img :src="anime.entry[0].images.jpg.image_url" class="shadow-xl rounded-2xl h-40 w-40 bg-center ">
        <div class="font-mono text-xs absolute bottom-5 left-0 text-white">
            {{ anime.entry[0].title }}
        </div>
    </div>
</template>

<script>
export default {
    props: ['anime']
}
</script>

<style>

</style>