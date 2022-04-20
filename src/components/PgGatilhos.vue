<template>
  <h3>EXERCICIO DE GATILHOS</h3>
  <p>Qual Seu Nome</p>
  <span>{{ nome }}</span>
</template>

<script>
//GATILHOS SAO METODOS Q PODEMOS USAR PARA ORGANIZAR A ORDEM DE INSERSAO OU EXTRAÇÃO DOS DADOS E ETC
export default {
  name: "PgGatilhos",
  data() {
    return {
      nome: "Espere vai aparecer",
    };
  },
  created() {
    setTimeout(() => {
      this.nome = "Anonimo";
    }, 1000);
  },
  mounted() {
     setTimeout(() => {
      this.nome = "Adriano";
    }, 2000);
  },
};
</script>