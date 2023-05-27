<template>
  <div id="list">
    <h1>List of todos:</h1>
    <ul>
      <li v-for="(todo, index) in todos">{{ index+1 }} {{ todo }} <button @click='remove(index)'>remove</button></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'List',
  props: ['todos'],
  methods: {
    remove(index) {
      this.$emit('removeFromList', index);
    }
  }
};
</script>
