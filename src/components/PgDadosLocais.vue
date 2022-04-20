<template>
  <h3>TESTANDO DADOS DE COMPONENTES LOCAIS</h3>
  <p>Nome: {{ nome }} (teste de varavel )</p>
  <p>Idade: {{ idade }} (teste de varavel )</p>
  <p>Idade: {{ cpf }} (teste de varavel )</p>
</template>

<script>
export default {
  name: "PgDadosLocais",
  data() {
    return {
      nome: "Adriano",
      idade: 17,
      cpf: '058093445566'
    }
  }
}
</script>
