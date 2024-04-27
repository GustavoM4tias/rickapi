<template>
  <div class="container-fluid">
    <div class="row justify-content-center">
      <div
        class="card card-personagens col-lg-8 col-md-10 col-sm-10 m-5 justify-content-center align-items-center"
      >
        <div class="row">
          <div class="col-md-6 col-sm-12">
            <img
              class="card-img imagem"
              src="../assets/img/gustavodiniz.png"
              alt="Foto Gustavo"
            />
          </div>
          <div class="col-md-6 col-sm-12">
            <div class="card-body">
              <p class="card-text nome"><strong>Nome:</strong> Gustavo Diniz</p>
              <p class="card-text"><strong>Status:</strong> Alive</p>
              <p class="card-text"><strong>Espécie:</strong> Human</p>
              <p class="card-text"><strong>Gênero:</strong> Male</p>
              <p class="card-text"><strong>Local:</strong> Earth</p>
              <p class="card-text"><strong>RA:</strong> 1977490</p>
              <p class="card-text"><strong>Curso:</strong> 3º Termo C, ADS.</p>
              <p class="card-text"><strong>University:</strong> Unimar</p>
              <p class="card-text">
                Aparece em <strong>algumas</strong> aulas.
              </p>
              <div class="botoes">
                <a
                  href="https://github.com/GustavoM4tias/rickapi"
                  target="_blank"
                  class="btn btn-dark m-2"
                  ><i class="bi bi-github"></i> Github</a
                >
                <a href="#" target="_blank" class="btn btn-primary"
                  ><i class="bi bi-linkedin"></i> LinkedIn</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.nome {
  margin-top: 30px;
}

p {
  margin: 0 0 5px 10px;
}

.imagem {
  object-fit: cover;
  border-radius: 15px;
  box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.1);
  height: 60vh;
  transform: scaleX(-1);
}

.card-personagens {
  box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.1);
  transition: 0.3s;
  height: 70vh;
}

.card-personagens:hover {
  transform: scale(1.02);
  transition: 0.3s;
}

@media only screen and (max-width: 600px) {
  .imagem {
    margin-top: 15px;
    object-fit: cover;
    border-radius: 15px;
    box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.1);
    height: auto;
    transform: scaleX(-1);
  }

  .card-personagens {
    box-shadow: 1px 1px 5px rgba(0, 0, 0, 0.1);
    transition: 0.3s;
    height: auto;
  }
}
</style>
