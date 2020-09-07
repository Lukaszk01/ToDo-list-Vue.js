<template>
  <div>
    <form @submit.prevent="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add Todo...">
      <input type="submit" value="Submit" class="btn">
    </form>
  </div>
</template>

<script>
// import uuid from 'uuid';
export default {
  name: "AddTodo",
  data() {
    return {
      title: ''
    }
  },
  methods: {
    addTodo() {
      const newTodo = {
        title: this.title,
        completed: false
      }
      // Send up to parent
      this.$emit('add-todo', newTodo);
      this.title = '';
    }
  }
}
</script>

<style scoped>
  form {
    display: flex;
  }
  input[type="text"] {
    margin-top: 100px;
    margin-left: 100px;
    flex: 10;
    padding: 5px;
    height: 40px;
    font-size: 15px;
    border-radius-left: 5px;
    border: solid;
    border-color: #4b7f4b;
  }
  input[type="submit"] {
    margin-top: 100px;
    margin-right: 100px;
    height: 40px;
    border-radius-right: 5px;

    flex: 2;
  }
  .btn {
    background-color: #4b7f4b;
  }
  .btn:hover {
    background-color: #15d815;
  }
</style>
