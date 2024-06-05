<script setup>
// import logAvi from ~/data/logos/logoAvi.png"
const grupo = {
    nombre: "EduTLan",
    Facultad: "Educación y Ciencias Humanas",
    logo: "@/static/images/logoAvi.png",
    semilleros: [
        {
            nombre: "AVI",
            logo: "~/data/logos/logoAvi.png",
        },
        {
            nombre: "Laboratorio IA",
            logo: "~/data/logos/logoLabIA.jpg",
        }
    ]
}
</script>
<template>
    <h2>Componente Grupo</h2>
    <img alt="Logo" src="@/static/images/logoAvi.png" />
    <Card style="width: 25rem; overflow: hidden">
        <template #header>
            <img :alt="'Logo grupo' + grupo.name" :src="grupo.logo" />
        </template>
        <template #title>Grupo {{ grupo.nombre }}</template>
        <template #subtitle>{{ grupo.grupo }}</template>
        <template #content>
            <p v-for="semillero in grupo.semilleros">Semillero {{ semillero.nombre }}</p>
        </template>
        <template #footer>
            <div class="flex gap-3 mt-1">
                <Button label="Cancel" severity="secondary" outlined class="w-full" />
                <Button label="Save" class="w-full" />
            </div>
        </template>
    </Card>
</template>