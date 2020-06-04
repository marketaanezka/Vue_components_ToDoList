<template>
  <div class="list">
    <h2>To do List </h2>
      <TodoItem 
      v-for="(singletask, x) in taskArray"
      :task="singletask.task"
      :doBy="singletask.doBy"
      :key="x"
      />
  </div>
</template>

<script>
import TodoItem from './TodoItem.vue'
export default {
  components: {
    TodoItem: TodoItem,
  },
  name: 'App',
  data() {
    return {
      taskArray: [
        {task: "Buy coffee", 
        doBy: "Thursday"},
        {task: "Make coffee", 
        doBy: "Friday"},
        {task: "Charge headphones", 
        doBy: "Friday"},
        {task: "Focus on coding",
         doBy: "Saturday"},
        {task: "Submit homework", 
        doBy: "Sunday"},
      ]
    }
  }

};
</script>

<style lang="css">
* {
  box-sizing: border-box;
}

html {
  font-family: 'Courier New', Courier, monospace;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.list {
  background-color: #EEEEFF;
  text-align: center;
}
</style>
