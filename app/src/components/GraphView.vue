<script setup lang="ts">
  import { Plotly } from 'vue-plotly'

  const data = [{
          x: [1,2,3,4],
          y: [10,15,13,17],
          type:"scatter"
        }],
        layout = {
          title: "My graph"
        }
</script>

<template>
  <h1>Testando se o Plotly cria um gráfico</h1>

  <main>
    <Plotly :data="data" :layout="layout" :display-mode-bar="false"></Plotly>
  </main>
</template>

<style scoped>

</style>
