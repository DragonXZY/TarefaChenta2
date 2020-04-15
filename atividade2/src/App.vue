<template>
  <div id="app">
    <TodoForm :tarefas="tarefas" @AdicionarTexto="Adicionar($event)" />
    <TodoList :tarefas="tarefas"/>
  </div>
</template>

<script>
import TodoList from "./components/TodoList";
import TodoForm from "./components/TodoForm";

export default {
  name: "App",
  components: {
    TodoList,
    TodoForm
  },
  data: function() {
    return {
      tarefas: []};
  },
  methods: {
    Adicionar: function(event) {
      this.tarefas.push({
        texto: event.titulo,
        cor: event.cor
      })
      }
    }
}
</script>
<style>
</style>
