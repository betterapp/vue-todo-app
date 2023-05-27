<template>
  <div id="form">
  
  <input type="text" v-model='todo' /> <button @click='addTodo'>Add</button> 
  
  </div>
</template>

<script>
export default {
  name: 'Form',
  data() {
    return {
      todo: ''
    }
  },
  methods: {
    addTodo() {
      if (this.todo != '') {
        this.$emit('addTodo', this.todo);
        this.todo = '';
      }
    }
  },
};
</script>
