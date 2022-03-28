<template>
<div>
    <label for="tareaInput">Ingrese su nueva tareas</label>
    <input type="text" v-model="tarea" id="tareaInput">
    <p :style="{color: isCorrect}">El input no puede estar vacio</p>
    <button :disabled="tarea === ''" @click="agregarTarea(tarea)">Agregar</button>
</div>
</template>

<script>
export default {
    props: {
        agregarTarea: Function
    },
    data () {
        return {
            tarea: ""
        }
    },
    computed: {
        isCorrect() {
            return this.tarea === "" ? "#ff0000" : "#fff";
        }
    }
}
</script>

<style>

</style>