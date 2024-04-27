<script setup>
const personagem = defineProps(["name", "url", "status", "species", "gender", "location", "episode"])
const personagemId = personagem.url.split('/')[5]
const imageUrl = "https://rickandmortyapi.com/api/character/avatar/" + personagemId + ".jpeg" 

let colorStatus = ''

switch (personagem.status) {
    case "Alive":
        colorStatus = "darkgreen"
        break;
    case "Dead":
        colorStatus = "darkred"
        break;
    default:
        colorStatus = "darkblue"
        break;
}

</script>

<template>
    <div class="col-md-3 col-sm-6 p-2">
        <div class="card p-2 card-personagens">
            <img class="img-personagem p-2" :src="imageUrl" alt="Personagem" style="border-radius: 15px;">
            <div class="col-12">
                <p class="text-start small" style="margin-top: 15px;"><strong>Nome: </strong>{{personagem.name}}</p>
                <p class="text-start small status"><strong>Status: </strong><strong :style="{ color: colorStatus}"> {{personagem.status}}</strong></p>
                <p class="text-start small"><strong>Espécie: </strong>{{personagem.species}}</p>
                <p class="text-start small"><strong>Gênero: </strong>{{personagem.gender}}</p>
                <p class="text-start small"><strong>Local: </strong>{{personagem.location}}</p>
                <p class="text-start small">Aparece em <strong>{{personagem.episode}}</strong> episódios.</p>
            </div>
        </div>
    </div>
</template>
