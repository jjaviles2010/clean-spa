<template>
  <div class="main-content centralizado">
    <h2 class="title is-2">Sobre o Clean.</h2>
      <br />
     <ul class="corpo">
        <li>O Clean é um projeto desenvolvido por uma equipe da turma 18 Mob da Fiap.</li>
        <li>A nossa equipe decidiu trabalhar no projeto após passar por diversas dificuldades para contratar uma diarista.</li>
        <li>O Clean é um aplicativo que vai ajudar você encontrar uma diarista de confiança.</li>
        <li>Nunca mais você vai sofrer pra achar alguem que cuide da limpeza da sua casa.</li>
        <li>Mostramos as profissionais perto da sua região.</li>
        <li>Antes de contratar você poderá verificar as avaliações das professionais e os comentarios de clientes anteriores.</li>
      </ul>
      <p class="store_text">Você pode baixar o novo aplicativo acessando à loja:</p>
      <div>
          <div class="app_store_image">
            <img src="~/assets/downloadAppStore.png">
          </div>
          <div class="google_play_image">
            <img src="~/assets/downloadGooglePlay.png">
          </div>
      </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'About'
  }
}
</script>

<style scoped>
.centralizado {
  text-align: center;
  margin: 0 100px;
  padding: 50px;
}

.corpo {
  font-family: Helvetica, Arial, sans-serif;
  width: 96%;
  color: gray;
  font-weight: bold
}

.lista-fotos {
  list-style: none;
}

.lista-fotos .lista-fotos-item {
  display: inline-block;
}

.store_text {
  font-family: Helvetica, Arial, sans-serif;
  padding-top: 15%;
  width: 96%;
  color: black;
  font-weight: bold
}

.app_store_image {
  float: left;
  width: 30%;
  text-align: center;
  padding-left: 12%;
  margin-left: 15%;
  margin-top: 2%;
}

.google_play_image {
  float: right;
  width: 30%;
  text-align: center;
  padding-right: 12%;
  margin-right: 20%;
  margin-top: 2%;
}

</style>
