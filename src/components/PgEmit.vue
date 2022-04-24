<!--EMIT FAZ O INVERSO DOS PROPS:
TIPO:  
PROPS JOGA OS DADOS PARA O COMPONENTE FILHO
EMIT ESCUTA O Q ESTA ACONTECENDO NOS EVENTOS DO FILHO E EXECULTA OS METODOS DO PAI-->
<template>
  <h3>APRENDENDO EMIT</h3>
  <button @click="$emit('mudarImagem')">Mudar Imagem</button>
</template>

<script>
export default {
  name: "PgEmit",
  emit: ["mudarImagem"],
};
</script>

<style>
</style>