<template>
  <div id="app">
    <header-component :header="header.toLocaleUpperCase()"/>
    <form-component @addTodo="addTodo"/>
    <todo-list-component :todos="todos"/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import HeaderComponent from './components/Header.vue';
import FormComponent from './components/Form.vue';
import TodoListComponent from './components/TodoList.vue';

export default Vue.extend({
  name: 'app',
  components: {
    HeaderComponent,
    FormComponent,
    TodoListComponent,
  },
  data() {
    return {
      header: 'Todo list',
      todos: [
        'Learn Vue',
        'Plan next trip',
        'Go shopping',
      ],
    };
  },
  methods: {
    addTodo(newTodo: string) {
      if (newTodo.length > 0) {
        this.todos.push(newTodo);
      }
    },
  },
});
</script>
