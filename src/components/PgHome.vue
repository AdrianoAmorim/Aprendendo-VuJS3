<template>
  <h1>EXERCICIOS VUEJS 3</h1>
  <PgDadosLocais />
  <br />
  <PgDataBinding />
  <br />
  <PgGatilhos />
  <br />
  <PgDiretivas />
</template>

<script>
import PgDadosLocais from "./PgDadosLocais.vue";
import PgDataBinding from "./PgDataBinding.vue";
import PgGatilhos from "./PgGatilhos.vue";
import PgDiretivas from "./PgDiretivas.vue";
export default {
  name: "PgHome",
  components: {
    PgDadosLocais,
    PgDataBinding,
    PgGatilhos,
    PgDiretivas,
  },
};
</script>


