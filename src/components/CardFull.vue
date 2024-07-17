<script setup></script>

<template>
  <div class="card">
    <div class="header">
      <slot name="header"></slot>
    </div>
    <slot>Corpo Padrão do card</slot>
    <div v-if="$slots.footer">
        <p>Mais informações abaixo...</p>
    </div>

    <div v-if="$slots.footer" class="footer">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<style scoped>
.card {
  height: 200px;
  width: 400px;
  box-shadow: 2px 2px 3px 3px gray;
  border-radius: 20px;
  padding: 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.header {
  background-color: greenyellow;
  height: 60px;
  width: 100%;
  border-radius: 20px;
}

.footer {
    background-color: greenyellow;
    height: 60px;
    width: 100%;
    border-radius: 20px;
  }

</style>
