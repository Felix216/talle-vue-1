<template>
    <div>
        <input type="text" placeholder="Tarea">
        <button @click="agregarTarea">Agregar Tarea</button>
        <ul>
            <li> {{contenido}} </li>
        </ul>
    </div>
</template>

<script setup>
    import { ref } from 'vue';

    const contenido = ref("");
    const agregarTarea = () => {
        
    }
</script>

<style scoped>

</style>