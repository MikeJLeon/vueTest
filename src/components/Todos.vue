<template>
  <div>
    <div class="todoRow" v-bind:key="todo.id" v-for="todo in todos">
      <h3><Todoitem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)"/></h3>
    </div>
  </div>
</template>
<script>
import Todoitem from "./Todoitem.vue";

export default {
  name: "Todos",
  components:{
      Todoitem,
  },
  props: ["todos"],
  
};
</script>
<style scoped>
h3{
    background-color:rgb(230, 230, 230);
}
</style>