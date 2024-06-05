<script setup>
const props = defineProps(
    {
        grupo: Object,
    }
)

</script>
<template>
    <Card style="width: 25rem; overflow: hidden">
        <template #title>Grupo {{ grupo.nombre }}</template>
        <template #content>
            <p v-for="semillero in grupo.semilleros">Semillero {{ semillero }}</p>
        </template>
        <template #footer>
            <div class="flex gap-3 mt-1">
                <Button label="Cancelar" severity="secondary" outlined class="w-full" />
                <Button label="Guardar" class="w-full" />
            </div>
        </template>
    </Card>
</template>