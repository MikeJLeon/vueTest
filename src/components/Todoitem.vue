<template>
  <div class="todo" v-bind:class="{'is-complete':todo.completed}">
    <input type="checkbox" v-on:change="markComplete">
    <p>{{ todo.title }}</p>
    <button @click="$emit('del-todo', todo.id)" class="del"/>
  </div>
</template>

<script>
export default {
  name: "Todoitem",
  props: ["todo"],
  methods: {
      markComplete(){
          this.todo.completed = !this.todo.completed;
      }
  }
};
</script>

<style scoped>
.todo{
    display:flex;
    align-items: center;
    gap: 50px;
}
.todo button{
    width:50px;
    height:25px;
    background-color:Red;
}
</style>