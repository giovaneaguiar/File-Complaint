<template>
  <div id="app">
    <h1>Registrar Reclamação</h1>
    <div class="conteudo">
      <form class="painel">
        <div class="cabecalho">Formulário</div>
        <Rotulo nome="E-mail">
          <input type="text" />
        </Rotulo>
        <Escolha></Escolha>
      </form>
    </div>
  </div>
</template>

<script>
import Rotulo from "./components/Rotulo.vue";
import Escolha from "./components/Escolha.vue";

export default {
  name: "App",
  components: {
    Rotulo,
    Escolha,
  },
};
</script>

<style>
body {
  background: #dae2f8;
  background: -webkit-linear-gradient(to right, #d6a4a4, #dae2f8);
  background: linear-gradient(to right, #d6a4a4, #dae2f8);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  margin-top: 60px;
}

.conteudo {
  display: flex;
}
.painel {
  flex: 1;
  background: #fff;
  margin: 0px 10px;
  padding: 20px;
  border: 1px solid #aaa;
  border-radius: 5px;
}

.painel .cabecalho {
  width: 100%;
  background-color: #ddd;
  padding: 10px 0px;
  border-radius: 5px;
  font-size: 1.4rem;
}

#app h1 {
  font-weight: 300;
  margin: 20px;
  padding: 0;
}
</style>
