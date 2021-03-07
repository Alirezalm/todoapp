<template>
  <div id="app">
    <h3>To Do List</h3>
    <ul>
      <li>
        <to-do-item label="my todo list" :done="false"></to-do-item>
      </li>
    </ul>
  </div>
</template>

<script>


import ToDoItem from "@/components/ToDoItem";

export default {
  name: 'App',
  components: {ToDoItem},
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
