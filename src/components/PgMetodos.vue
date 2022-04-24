<template>
  <h3>EXERCICIO METODOS</h3>
  <p>
    Clique no Botao para aparecer a imagem
    <button @click="showImg">Mostrar Imagem</button>
    <img id="peppa" v-show="status" :src="urlImg" alt="imgPeppa" />
  </p>
  <p>
    <PgProps :urlImg="urlImg" compUrlImg="/img/Peppa.png"/>
  </p>
</template>

<script>
import PgProps from "./PgProps.vue";
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
  components: {
    PgProps,
  },
};
</script>
<style scoped>
img {
  max-width: 8%;
  max-height: 8%;
}
</style>