<!--PODEMOS PASSAR OS PROPS (DADOS) ATRAVES DA PARTE PROPS NO EXPORT DEFAULT 
PEGAMOS OS DADOS DO PAI ATRAVES DE UM BIND COM A VARIAVEL DO DATA(), E TMB PASSANDO 
DIRETO O VALOR NA PROPRIA TAG HTML DO COMPONENTE
(SE FOR PASSAR VALOR BOOLEAN TEMOS Q FAZER BIND) NO CASO DE PASSAR VALORES DIRETAMENTE-->
<template>
  <h3>Utilizando PROPS</h3>
  <p>
    Essa Imagem apareceu usando uma Props com Bind em Dados vindo do Data !!!
    <img :src="urlImg" alt="oi" />
    <br/>
    Essa Imagem apareceu usando uma Props com dados diretamente via tag html !!!
     <img :src="compUrlImg" alt="oia" />
  </p>
</template>

<script>
export default {
  name: "PgProps",
  props: {
    urlImg: String,
    compUrlImg: String
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
img {
  max-width: 8%;
  max-height: 8%;
}
</style>