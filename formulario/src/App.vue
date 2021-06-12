<template>
  <div id="app">
    <h1>Registrar Reclamação</h1>
    <div class="conteudo">
      <form class="painel">
        <div class="cabecalho">Formulário</div>
        <Rotulo nome="E-mail">
          <input type="text" />
        </Rotulo>
        <Rotulo nome="Senha">
          <input type="password" />
        </Rotulo>
        <Rotulo nome="Idade">
          <input type="number" />
        </Rotulo>
        <Rotulo nome="Mensagem">
          <textarea name="" cols="20" rows="5"></textarea>
        </Rotulo>
        <Rotulo nome="Características do Problema">
          <span class="mr-4"
            ><input type="checkbox" value="reproduzivel" /> Reproduzível</span
          >
          <span
            ><input type="checkbox" value="intermitente" /> Intermitente</span
          >
        </Rotulo>
        <Rotulo nome="Qual produto?">
          <span class="mr-4"><input type="radio" /> Web</span>
          <span class="mr-4"><input type="radio" /> Mobile</span>
          <span><input type="radio" /> Outro</span>
        </Rotulo>
        <Rotulo nome="Prioridade">
          <select name="" id="">
            <option></option>
          </select>
        </Rotulo>
        <Rotulo nome="Primeira Reclamação?">
          <Escolha />
        </Rotulo>
        <hr />
        <button>Enviar</button>
      </form>
      <div class="painel">
        <div class="cabecalho">Resultados</div>
      </div>
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
#app form button {
  background-color: #d6a4a4;
  font-size: 1.5rem;
  border-radius: 5px;
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

.mr-4 {
  margin-right: 40px;
}
</style>
