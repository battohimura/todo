<template>
<div>
    <p v-if="tareasCreadas.length === 0"> La lista esta vacia </p>
    <ul v-else>
        <li v-for="(tarea, index) in tareasCreadas" :key="index">{{tarea}}</li>
    </ul>
</div>
</template>

<script>
export default {
    props: {
        tareasCreadas: Array
    }
}
</script>

<style>

</style>
