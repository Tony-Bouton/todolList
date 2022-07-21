<template>
  <div class="wrapper">
    <form action="" @submit.prevent="addTask">
      <label for="todo">Nouvelle tache</label>
      <input type="text" name="todo" id="todo" v-model="newTask" />

      <input type="submit" value="Ajouter" @click="update" />
    </form>
  </div>

  <option-task :taskList1="taskList"></option-task>

  <ul>
    <display-task
      v-for="(item, index) in taskList"
      :key="index"
      :todo="item"
      :taskList1="taskList"
      :index="index"
      :id="index"
    >
    </display-task>
  </ul>
</template>

<script>
import displayTask from "./displayTask.vue";
import OptionTask from "./OptionTask.vue";

export default {
  components: { displayTask, OptionTask },
  data() {
    return {
      newTask: "",
      taskList: [],
    };
  },

  props: {
    todo: {
      type: String,
    },
    taskList1: {
      type: Array,
    },
    index: {
      type: String,
    },
  },

  methods: {
    addTask: function () {
      this.taskList.push(this.newTask);
      this.newTask = null;
    },
  },
};
</script>

<style></style>
