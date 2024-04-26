<script setup>
import { onMounted, ref } from "vue";
import ListPersonagens from "../components/ListPersonagens.vue";

let personagens = ref([]);
const contador = ref(1);

const fetchPersonagens = () => {
  const url = `https://rickandmortyapi.com/api/character/?page=${contador.value}`;
  fetch(url)
    .then((response) => response.json())
    .then((response) => {
      personagens.value = response.results;
      console.log(personagens);
    });
};

onMounted(fetchPersonagens);

const nextPage = () => {
  if (contador.value < 42) {
  contador.value++;
    personagens.value = [];
  fetchPersonagens();
  window.scrollTo({
    top: 0,
    behavior: "smooth"
  });
  }
};

const backPage = () => {
  if (contador.value > 1) {
    contador.value--;
    personagens.value = [];
    fetchPersonagens();
  }
};
</script>

<template>
  <main>
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
                :episode="personagem.episode.length"
              />
            </div>
          </div>
        </div>
      </div>
    <div class="p-2">
      <p class="text-center">Pagina: {{ contador }}</p>
      <div class="d-flex justify-content-center">
        <button class="btn btn-secondary m-1 p-1" @click="backPage">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        </button>
        <button class="btn btn-secondary m-1 p-1" @click="nextPage">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
        </button>
      </div>
    </div>
    </div>
  </main>
</template>
