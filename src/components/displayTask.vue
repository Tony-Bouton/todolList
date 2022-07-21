<template>
  <ul>
    <li v-for="(item, index) in todolist" :key="index">
      {{ todo }}
    </li>
  </ul>
</template>

<script setup>
import { useTask } from "./CreateTask.vue";
const { todo, todoList } = useTask();
console.log(todo);
console.log(todoList);
</script>

<style></style>
