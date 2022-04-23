<template>
  <h3>DATA BINDING</h3>

  <form id="formulario" @submit.prevent="pegarValor">
    <!-- O v-modelo recebe o nome da variavel para fazer o binding   -->
    <!--PODE COLOCAR O @ NO LUGAR DO V-ON (NOME DO BINDING), prevent (previne manda os dados p formulario) -->
    <span
      >Nome:
      <input type="text" v-model="input_name" placeholder="Digite seu Nome" />
    </span>
    <input type="submit" value="enviar" />
  </form>

  <p>Binding Dinamico com o campo Nome: {{ input_name }}</p>
  <p>Binding Estático com o campo Nome: {{ input_estatico }}</p>
</template>

<script>
export default {
  name: "PgDataBinding",
  data() {
    return {
      input_name: "",
      input_estatico: "",
    };
  },
  methods: {
    pegarValor() {
      this.input_estatico = this.input_name;
    },
  },
};
</script>