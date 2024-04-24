<script setup> 
const personagem = defineProps(["name", "url", "status", "species", "gender", "location"])
const personagemId = personagem.url.split('/')[5]
const imageUrl = "https://rickandmortyapi.com/api/character/avatar/" + personagemId + ".jpeg" 

</script>

<template>
    <div class="col-md-3 col-sm-6 p-2">
        <div class="card p-2" style="box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.1);">
            <img :src="imageUrl" alt="Personagem" style="border-radius: 5px;">
            <p class="text-start ">Nome: {{personagem.name}}</p>
            <p class="text-start ">Status: {{personagem.status}}</p>
            <p class="text-start ">Espécie: {{personagem.species}}</p>
            <p class="text-start ">Genero: {{personagem.gender}}</p>
            <p class="text-start ">Local: {{personagem.location}}</p>
        </div>
    </div>
</template>

<style>

</style>

