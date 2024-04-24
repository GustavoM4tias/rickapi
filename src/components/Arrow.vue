<script setup>
import { ref } from "vue";

const contador = ref(1);

const proximaPagina = () => {
  contador.value++;
};

const voltaPagina = () => {
  if (contador.value > 1) {
    contador.value--;
  }
};
</script>

<template>
    <div>
      <p class="text-center">Pagina: {{ contador }}</p>
      <div class="d-flex justify-content-center">
        <button class="btn btn-secondary m-1 p-1" @click="voltaPagina">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        </button>
        <button class="btn btn-secondary m-1 p-1" @click="proximaPagina">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
        </button>
      </div>
    </div>
</template>
