    <!-- diretivas condicionais  - variavel vazia testa se tem alguma coisa
  retorna true sempre q houver algo (texto, numero ou true) so retorna false se 
  for null ou false -->
    <!-- Diretiva v-show, testa se a variavel e true mostra o conteudo .. 
  se for false nao mostra -->
<template  >
  <h3>DIRETIVAS NO VUEJS (V-IF , V-ELSE,V-SHOW) e modo emit</h3>
  <div class="backgroundBlue">
    <span>DIGITE SEU NOME:</span>
    <input type="text" v-model="inNome" placeholder="Digite seu Nome" />
    <input type="submit" value="Enviar" @click="getNome" />

    <p>Oi meu nome é: {{ nome }}</p>
    <p>Estado de Ocupação:</p>

    <p v-if="status === ''">...</p>
    <p v-else-if="status == false">Infelismente esta pessoa esta ocupada !!</p>
    <p v-else-if="status == 'celular'">
      Infelismente esta pessoa esta ocupada NO CELULAR!!
    </p>
    <p v-else-if="status == true">
      LIBERADO PARA BRINCAR!! PAPAI te AMa
      <img id="peppa" v-show="status" :src="urlImg" alt="imgPeppa" />

      <PgEmit @mudar-Imagem="trocarImagem" />
    </p>
    <p v-else>ESTA PESSOA NAO ESTA CADASTRADO NA BASE DE DADOS.</p>
  </div>
</template>

<script>
import PgEmit from "./PgEmit.vue";

export default {
  name: "PgDiretivas",
  data() {
    return {
      urlImg: "/img/Peppa.png",
      status: "",
      nome: "",
      inNome: "",
    };
  },
  methods: {
    pesquisaNome() {
      if (this.nome == "adriano") {
        this.status = false;
      } else if (this.nome == "cristiane") {
        this.status = "celular";
      } else if (this.nome == "alice") {
        this.status = true;
      } else {
        this.status = null;
      }
    },
    getNome() {
      this.nome = this.inNome;
      this.pesquisaNome();
    },
    trocarImagem() {
      this.urlImg = '/img/Lol.png'
    },
  },

  components: {
    PgEmit,
  },
};
</script>

<style scoped>
img {
  max-width: 8%;
  max-height: 8%;
}
</style>