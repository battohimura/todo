<template>
  <div class="home">
    <!-- 3. Uso de componente -->
    <CrearNuevasTareas :agregarTarea="agregarTarea"/>
    <hr />
    <ListaDeTareas :tareasCreadas="tareas" />
  </div>
</template>

<script>
// @ is an alias to /src
import ListaDeTareas from "@/components/ListaDeTareas.vue"; // 1. Importar componente
import CrearNuevasTareas from "@/components/CrearNuevasTareas.vue";
export default {
  name: "HomeView",
  components: {
    ListaDeTareas, // 2. Declarar/registrar que componentes vas a utilizar en la vista/componente
    CrearNuevasTareas,
  },
  data() {
    return {
      tareas: [],
    };
  },
  methods: {
    agregarTarea(tarea) {
      this.tareas.push(tarea);
    }
  }
};
</script>
