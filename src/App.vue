<script setup>
import { ref } from "vue";
import ExpandBox from "./components/ExpandBox.vue";

const caixas = [
  {id: 1, title: 'Caixa 1'},
  {id: 2, title: 'Caixa 2', qtde: 20},
  {id:3, title: 'Caixa 3', content:'Conteúdo secreto da caixa 3'},
  {id:4, title: 'Caixa 4', content: 'Conteúdo da caixa', qtde: 5}
]


const mostrarSenha = ref(false)

function trocarSenha() {
  if (mudarSenha.value == "password"){
    mudarSenha.value = "text"
  }
  else{
    mudarSenha.value = "password"
  }

} 
</script>


<template>

  <label>
    <button @click="mostrarSenha = !mostrarSenha">Visualizar senha</button>
    <input :type="mostrarSenha ? 'text' : 'password' ">
  </label>

  <expand-box v-for="caixa in caixas" :key="caixa.id" v-bind="caixa" />
</template>

<style scoped>

</style>
