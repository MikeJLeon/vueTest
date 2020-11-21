<template>
  <header class="header">
    <h1>Todo List</h1>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>
<style scoped>
.header h1 {
  background-color: black;
  color: White;
  margin: 0;
  padding: 20px;
  text-align: center;
}
</style>