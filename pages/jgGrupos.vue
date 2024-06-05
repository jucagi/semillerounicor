<script setup>
const grupo = {
    nombre: "EduTLan",
    Facultad: "Educación y Ciencias Humanas",
    semilleros: [
            "AVI",
            "Laboratorio IA",
    ]
}
</script>

<template>
    <h1>Grupos</h1>
    <JgGrupo :grupo="grupo" />
</template>
