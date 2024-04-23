<template>
  <div>
        <h1>Lista de tareas</h1>
        <input type="text" placeholder="Agrega una tarea" v-model="contenido">
        <button class="btn-blue" @click="agregarTarea">Agregar Tarea</button>
        <button class="btn-red" @click="quitarTarea">Quitar Tarea</button>
        <li v-for="tarea in tareas" :key="tarea.id">
          {{ tarea.value }}
        </li>
    </div>
</template>

<script setup>
  import { ref } from 'vue';

  const tareas = ref([]);
  const contenido = ref("");
  const agregarTarea = () => {
    tareas.value.push(contenido.value);
    contenido.value = "";
  }
  const quitarTarea = () => {
    tareas.value.pop();
  }
</script>

<style scoped>
  *{
    font-family: Arial, Helvetica, sans-serif;
  }
  input {
    padding: 16px;
    border-radius: 10px;
    border: none;
    background-color: #f3f3f3;
    margin-right: 12px
  }
  .btn-blue {
    padding: 16px;
    background-color: rgb(23, 119, 202);
    border: none;
    border-radius: 10px;
    color: white;
    margin-right: 12px;
  }
  .btn-red {
    padding: 16px;
    background-color: rgb(202, 23, 23);
    border: none;
    border-radius: 10px;
    color: white;
  }
</style>
