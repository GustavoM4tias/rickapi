<template>
  <div class="container-fluid d-flex justify-content-center tela">
    <div class="col-4 p-5">
    <div class="card p-1 card-personagens">
      <img class="imagem p-1" src="../img/gustavo.png" alt="Foto Gustavo" />
      <div class="col-12">
        <p class="text-start small" style="margin-top: 15px">
          <strong>Nome: </strong> Gustavo Diniz "Smith"
        </p>
        <p class="text-start small status">
          <strong>Status: </strong> Alive (ainda bem)
        </p>
        <p class="text-start small">
          <strong>Espécie: </strong> Human
        </p>
        <p class="text-start small">
          <strong>Gênero: </strong> Male
        </p>
        <p class="text-start small">
          <strong>Local: </strong> Earth
        </p>
        <p class="text-start small">
          <strong>RA: </strong> 1977490
        </p>
        <p class="text-start small">
          <strong>Curso: </strong> 3º Termo C, ADS.
        </p>
        <p class="text-start small">
          <strong>University: </strong> Unimar 
        </p>
        <p class="text-start small">
          Aparece em <strong>algumas</strong> aulas.
        </p>
      </div>
    </div>
  </div>
  </div>
</template>

<style>

p{
    margin: 0 0 5px 10px;
}

.imagem {
  object-fit: cover;
  width: 300px;
  border-radius: 15px;
}

.card-personagens {
    box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.1);
    transition: 0.3s;
}

.card-personagens:hover {
    transform: scale(1.02);
    transition: 0.3s;
}

</style>
