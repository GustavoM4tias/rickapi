<script setup>
import { onMounted, ref } from "vue";
import ListPersonagens from "../components/ListPersonagens.vue";
import Arrow from "../components/Arrow.vue";

let personagens = ref([]);
let valor = 1;
let url = "https://rickandmortyapi.com/api/character/?page=" + valor;

onMounted(() => {
  fetch(url)
    .then((response) => response.json())
    .then((response) => {
      personagens.value = response.results;
      console.log(personagens);
    });
});


const contador = ref(0);

console.log(contador)
</script>

<template>
  <main style="margin-bottom: 70px">
    <div class="container-fluid">
      <div class="row mt-4 d-flex justify-content-center">
        <div class="col-md-12">
          <div class="card">
            <div class="card-body row">
              <ListPersonagens
                v-for="personagem in personagens"
                :key="personagem.name"
                :name="personagem.name"
                :url="personagem.url"
                :status="personagem.status"
                :species="personagem.species"
                :gender="personagem.gender"
                :location="personagem.location.name"
              />
            </div>
          </div>
        </div>
      </div>
      <Arrow :contador="contador"/>
    </div>
  </main>
</template>

