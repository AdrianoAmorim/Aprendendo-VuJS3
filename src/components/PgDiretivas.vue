<template>
  <h3>DIRETIVAS NO VUEJS (V-IF , V-ELSE,V-SHOW)</h3>
  <div>
    <span>DIGITE SEU NOME:</span>
    <input type="text" v-model="inNome" placeholder="Digite seu Nome" />
    <input type="submit" value="Enviar" @click="getNome" />
  </div>
  <p>Oi meu nome é: {{ nome }}</p>
  <p>Estado de Ocupação:</p>

  <p v-if="status === ''">...</p>
  <p v-else-if="status == false">Infelismente esta pessoa esta ocupada !!</p>
  <p v-else-if="status == 'celular'">
    Infelismente esta pessoa esta ocupada NO CELULAR!!
  </p>
  <p v-else-if="status == true">LIBERADO PARA BRINCAR!! PAPAI te AMa</p>
  <p v-else>ESTA PESSOA NAO ESTA CADASTRADO NA BASE DE DADOS.</p>
</template>

<script>
export default {
  name: "PgDiretivas",
  methods: {
    pesquisaNome() {
      if (this.nome == "adriano") {
        this.status = true;
      } else if (this.nome == "cristiane") {
        this.status = "celular";
      } else if (this.nome == "alice") {
        this.status = false;
      }
      else {
        this.status = null;
      }
    },
    getNome() {
      this.nome = this.inNome;
      this.pesquisaNome();
    },
  },
  data() {
    return {
      status: "",
      nome: "",
      inNome: "",
    };
  },
};
</script>

<style>
</style>