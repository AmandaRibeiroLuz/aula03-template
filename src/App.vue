<script setup>
const nome = prompt(`Informe o seu nome.`);
const idade = Number(prompt(`Informe a sua idade.`));

function inverter(texto) {
  return texto.split('').reverse().join('');
}

function saudacao() {
  return `Olá, ${nome}!`
}

function incrementar() {
  contador.value++
}

function decrementar() {
    contador.value--
  
}

</script>

<template>
  <div class="info">
    
    <h1>Exemplo 1 - Mostrando informações na tela:</h1>
    <p>Nome: {{ nome }}.</p>
    <p>Idade: {{ idade }} anos.</p>
    <hr />
    <p>Para completar 50 anos faltam: {{ 50 - idade }} anos.</p>
    <p>O nome tem {{ nome.length }} caracteres.</p>
    <p>O nome invertido é: {{ inverter(nome) }}.</p>
    <p>O nome invertido em letras maiúsculas é: {{ inverter(nome).toUpperCase() }}</p>
    <hr />
    <p> Exemplo de saudação usando função:</p>
    <p> {{ saudacao() }} </p>

  </div>
  <div class="contador">

    <h2>Contador:</h2>
    <p>Valor: {{ contador }} </p>
    <button v-on:click="incrementar">+</button>
    <button @click="decrementar">-</button>

    <div v-if="contador > 10">O valor é maior que 10.</div>
    <div v-else>O valor é menor que 10.</div>

  </div>
</template>

<style scoped>
.info {
  background-color: #91c2ebbb;
  padding: 20px 30px;
  color: rgb(0, 0, 0);
  border-radius: 10px;
}
.contador {
  background-color: #91c2ebbb;
  padding: 20px 30px;
  margin: 1vw 0;
  color: rgb(0, 0, 0);
  border-radius: 10px;
}
h1 {
  color: rgb(0, 23, 58);
  font-weight: bold;
  font-size: 1.5rem;
}
h2 {
  color: rgb(0, 23, 58);
  font-weight: bold;
  font-size: 1.5rem;
}
button {
  padding: 5px 15px;
  margin: 5px;
  background-color: #6db3ecbb;
  color:  rgb(9, 67, 153);
  border-radius: 5px;
}
</style>
