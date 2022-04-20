<template>
  <h3>DIRETIVAS NO VUEJS (V-IF , V-ELSE,V-SHOW)</h3>
  <div>
    <span>DIGITE SEU NOME:</span>
    <input type="text" v-model="inNome" placeholder="Digite seu Nome" />
    <input type="submit" value="Enviar" @click.prevent="getNome" />
  </div>
  <p>Oi meu nome é: {{ nome }}</p>
  <p>Estado de Ocupação:</p>
 
  <p v-if="status == ''">...</p>
  <p v-else-if="status">Infelismente esta pessoa esta ocupada !!</p>
  <p v-else-if="status == 'celular'">Infelismente esta pessoa esta ocupada NO CELULAR!!</p>
  <p v-else-if="!status">LIBERADO PARA BRINCAR!! PAPAI te AMa</p>
  <p v-else> ESTA PESSOA NAO ESTA CADASTRADO NA BASE DE DADOS.</p>
</template>

<script>
export default {
  name: "PgDiretivas",
  methods: {
    pesquisaNome() {
      if (this.nome == "adriano") {
   
        return true;
      } else if (this.nome == "cristiane") {
      
        return "celular";
      } else if (this.nome == "alice") {
       
        return false;
      }
    },
    getNome() {
      this.nome = this.inNome;
      this.status = this.pesquisaNome();
      console.log(this.status)
    }
  },
  data() {
    return {
      status: '',
      nome: "",
      inNome: "",
    };
  },
};
</script>

<style>
</style>