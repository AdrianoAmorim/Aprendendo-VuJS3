<template>
  <h3>EXERCICIO METODOS</h3>
  <p>
    Clique no Botao para aparecer a imagem
    <button @click="showImg">Mostrar Imagem</button>
    <img id='peppa' v-show="status" :src="urlImg" alt="imgPeppa" />
  </p>
</template>

<script>
export default {
  name: "PgMetodos",
  data() {
    return {
      status: false,
      urlImg: "/img/Peppa.png",
    };
  },
  methods: {
    showImg() {
      this.status = !this.status;
    },
  },
};
</script>
<style scoped>
img {
  max-width: 8%;
  max-height: 8%;
}
</style>