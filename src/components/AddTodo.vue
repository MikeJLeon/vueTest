<template>
  <div>
    <form @submit="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add todo" />
      <input type="submit" value="Submit" class="btn" />
    </form>
  </div>
</template>
<script>
//import {v4} from 'uuid';
export default {
    name:"AddTodo",
    data(){
        return{
            title:"",
        }
    },
    methods:{
        addTodo(e){
            e.preventDefault();
            const newToDo = {
                title: this.title,
                completed:false,
            }
            //Send to parent from here
            this.$emit('add-todo', newToDo);
            this.title = "";
        }
    }
}
</script>
<style scoped>
form {
  display: flex;
  gap: 50px;
}
.btn {
  width: 75px;
  height: 25px;
}
</style>