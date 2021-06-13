<template>
  <div
    class="escolha"
    @click="ligado = !ligado"
    :class="{ ligado, desligado: !ligado }"
  >
    <div v-if="ligado" class="botao"></div>
    <div v-else class="botao"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ligado: false,
    };
  },
};
</script>

<style scoped>
.escolha {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 15px;
  width: 40px;
  border-radius: 20px;
  border: 1px solid #aaa;
}

.botao {
  position: absolute;
  margin: 0px 5px;
  height: 25px;
  width: 25px;
  border-radius: 14px;
  background: #fff;
  box-shadow: 0px 0px 5px #000b;
}

.desligado {
  background-color: grey;
}

.ligado {
  background-color: grey;
}

.desligado .botao {
  left: -10px;
}

.ligado .botao {
  background-color: #d6a4a4;
  right: -10px;
}
</style>