
<template>
  <div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
    <p>
      <input type="checkbox" v-on:change="markComplete" v-bind:checked="todo.completed">
      {{todo.title}}
      <button @click="$emit('del-todo', todo.id)" class="del">Delete!</button>
      </p>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    }
  }
}
</script>

<style scoped>
  .todo-item {
    background: #4b7f4b;
    padding: 10px;
    border-bottom: 1px #ccc dotted;
    padding: 25px;
    margin: 50px;
    box-shadow: 1px 1px 3px grey;
    margin-left: 300px;
    margin-right: 300px;

  }
  .todo-item p {
    text-shadow: 0.9px 0.9px 0.9px black;
    font-size: 20px;
    margin-left: 5px;
    color: white;
    font-family: times new roman;
  }
  .is-complete {
    text-decoration: line-through;
  }
  .del {
    background: #ff0000;
    color: #fff;
    border: none;
    padding: 5px 9px;
    border-radius: 10%;
    cursor: pointer;
    float: right;
    height: 35px;
    width: 60px;
  }

</style>
