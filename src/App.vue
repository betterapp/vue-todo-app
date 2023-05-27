<template>
  <div id="app">
    <Form @add-todo="addToList" />
    <List :todos="todoList" @remove-from-list='removeFromList'/>
  </div>
</template>

<script>
import Form from './components/Form.vue';
import List from './components/List.vue';


export default {
  name: 'App',
  data() {
    return {
      todoList: [],
    };
  },
  methods: {
    addToList(todo) {
      this.todoList.push(todo);
    },
    removeFromList(index) {
      this.todoList.splice(index, 1)
    }
  },
  components: {
    Form,
    List
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
