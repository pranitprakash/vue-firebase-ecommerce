<template>
  <div class="about">
    <h1>This is an about page</h1>
    <Todo></Todo>
  </div>
</template>
<script>
// @ is an alias to /src

import Todo from "@/components/Todo.vue";


export default {
  name: "Home",
  components: {
 Todo
    
  }
};
</script>