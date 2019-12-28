<template>
        <div class="painel">
          <h2 class="painel-titulo">{{titulo}}</h2>
          <slot>
              <!-- Aqui será inserido conteudo dinamico-->
          </slot>
          <h1 class="painel-titulo">{{repositories}} repositorios no GitHub</h1>
        </div>
</template>

<script>
export default {
  props: ['titulo', 'repositories']
}
</script>

<style scoped>
.painel {
  padding: 0 auto;
  border: solid 1px grey;
  display: inline-block;
  margin: 0 10px;
  box-shadow: 2px 2px 10px grey;
  width: 150px;
  height: 100%;
  vertical-align: top;
  text-align: center;
}

.painel .painel-titulo {
  font-size: 14px;
  text-align: center;
  border-bottom: solid 1px #ffffff;
  background: #03A9F4;
  margin: 0;
  padding: 10px;
  text-transform: uppercase;

}
</style>
