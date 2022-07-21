<template>
  <div class="wrapper">
    <form action="" @submit.prevent="addTask">
      <label for="todo">Nouvelle tache</label>
      <input type="text" name="todo" id="todo" v-model="newTask" />

      <input type="submit" value="Ajouter" />
    </form>
  </div>

  <display-task></display-task>
</template>

<script>
import { ref } from "@vue/reactivity";
import displayTask from "./displayTask.vue";

export function useTask() {
  const todo = ref("0");
  const todoList = ref([0]);

  function update() {
    todo.value = this.newTask;
    todoList.value = this.taskList;
  }

  return { todo, todoList };
}

export default {
  components: { displayTask },
  data() {
    return {
      newTask: "",
      taskList: [],
    };
  },

  methods: {
    addTask: function () {
      this.taskList.push(this.newTask);
      console.log(this.taskList);
    },
  },
};
</script>

<style></style>
