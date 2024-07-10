<script setup>
import { ref, computed } from 'vue'

const props = defineProps(['title'])
const showContent = ref(false)
const textoBotao = computed(() => showContent.value ? 'Esconder' : 'Mostrar')
</script>

<template>
    <div>
        <button @click="showContent = !showContent">{{ textoBotao }}</button>
        <div v-if="showContent" class="expand-box">
            <h1>{{ props.title }}</h1>
            <p> Texto da caixa </p>
        </div>
    </div>
</template>

<style scoped>
.expand-box {
    height: 100%;
    padding: 20px;
    border: 1px solid black;
    border-radius: 5px;
    box-shadow: 3px 3px 2px 2px gray;
}
</style>
