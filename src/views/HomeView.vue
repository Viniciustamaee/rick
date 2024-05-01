<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListRick from '../components/card.vue'
let character = reactive(ref())

onMounted (()=>{
  fetch("https://rickandmortyapi.com/api/character/")
  .then(response => response.json())
  .then(response => {
    character.value = response.results
  });
})
</script>

<template>
  <main class='bg-black'>
    <div class="container">
            <div class="card-body row" >
                <ListRick
                v-for="character in character"
                :key="character.name"
                :name="character.name"
                :image="character.image"
                :gender="character.gender"
                :status="character.status"
                :species="character.species"
                :location="character.location.name"
                :episode="character.episode"
                />
            </div>
          </div>
  </main>
</template>



