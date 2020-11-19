<template>
  <div class="todo">
    <h1>{{ title }}</h1>

    <input type="text" class="todo-input"  v-model="currentTodoItem"/>
    <button v-on:click="saveTask">Save</button>
   

    <ul>
    <li v-for="(task,index) in todoList" :key="task" >{{task}} {{index}}  <h1 v-on:click="deleteTask(index)"
    >x</h1></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data(){
      return {
          title:"welcome enter your tasks ",
          currentTodoItem:"",
          todoList:[]
      }
  },
  methods:{
      saveTask(){
         this.todoList.push(this.currentTodoItem);
         this.currentTodoItem="";
      },
      deleteTask(toDelete){
          this.todoList.splice(toDelete,1);
        
          
      }

  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
