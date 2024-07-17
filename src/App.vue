<script setup>
import { ref } from 'vue'
import ExpandBox from './components/ExpandBox.vue'
import Card from './components/Card.vue'
import CardFull from './components/CardFull.vue'

const caixas = [
  { id: 1, title: 'Caixa 1' },
  { id: 2, title: 'Caixa 2', qtde: 20 },
  { id: 3, title: 'Caixa 3', content: 'Conteúdo secreto da caixa 3' },
  { id: 4, title: 'Caixa 4', content: 'Conteúdo da caixa', qtde: 5 }
]
</script>

<template>
<h1>Slots</h1>
<CardFull> Função:Professor 
  <template #header>
    <h1>Eduardo da Silva</h1>
    </template>
    <template #footer>
      link das redes sociais
    </template>
</CardFull>
<CardFull> Função: Programador
  <template #header>
    <h1>Zé da Silva</h1>
  </template>
</CardFull>
<Card>Isabelle</Card>
<Card></Card>
<hr>
  <expand-box v-for="caixa in caixas" :key="caixa.id" v-bind="caixa" />
</template>

<style scoped></style>
