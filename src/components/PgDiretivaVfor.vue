<template>
  <h3>Exercicio sobre DIRETIVA V-FOR</h3>
<!-- a diretiva repete sempre o elemento q ela esta sendo usada.
 funciona sempre tendo q passar o Bind com o ID do objeto criado
 quando trabalhamos com array simples, usamos um segundo args (index) 
 sempre apos o nome do objeto criado pelo v-for -->
 <p>LISTAS DE CLIENTES:</p>
 <select name="slcClientes">
     <option v-for="Cliente in Clientes" :key="Cliente.id" value='{{Cliente.id}}'>
         {{Cliente.nome}}</option>
 </select>
  <ul>
    <li v-for="Cliente in Clientes" :key="Cliente.id">{{ Cliente.nome }}</li>
  </ul>
</template>

<script>
export default {
  name: "PgDiretivaVfor",
  data() {
    return {
      Clientes: [
        { id: 1, nome: "Adriano" },
        { id: 2, nome: "Alice" },
        { id: 3, nome: "Cristiane" },
        { id: 4, nome: "João" },
      ],
    };
  },
};
</script>

<style scoped>
li {
    list-style-type: none;
}

</style>
