<template>
  <header class="header">
    <h1>TodoList</h1>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style scoped>
  .header {
    background: #4b7f4b;
    color: #fff;
    text-align: center;
    padding: 10px;
    height: 100px;
  }
  .header a {
    color: #fff;
    padding-right: 5px;
    text-decoration: none;
    text-shadow: 0.5px 0.5px 0.5px black;
  }
  .header a:hover {
    color: #15d815;
  }
  .header h1 {
    text-shadow: 0.5px 0.5px 0.5px black;
  }
</style>
