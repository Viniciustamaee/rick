<script setup>
const character = defineProps(["name", "image", "gender", "status", "species", "location", "episode"]);
const qtdeEp = character.episode.length; 
</script>

<template> 
    <div class="card m-3 border border-3 " style="width: 18rem;">
      <img :src="character.image" class="card-img-top mt-2 w-100" alt="...">
      <div class="card-body">
        <h5 class="card-title text-center fs-4">{{ character.name }}</h5>
        <p class="card-text"><b>Gender:</b> {{ character.gender }}</p>
        <p class="card-text"><b>status:</b> {{ character.status }}</p>
        <p class="card-text"><b>species:</b> {{ character.species }}</p>
        <p class="card-text"><b>location:</b> {{ character.location }}</p>
        <p class="card-text"><b>Ep:</b> {{ qtdeEp}}</p>
      </div>
    </div>
    </template>
    

<style>


    .card-body {
        font-family:sans-serif;
        font-size: 17px;    
    }


</style>