<template>
  <!-- Créer une tâche  -->
  <form action="" @submit.prevent="addTask">
    <label for="todo">Nouvelle tache</label>
    <input type="text" name="todo" id="todo" v-model="newTask" />

    <input
      type="submit"
      value="Ajouter"
      @click="update"
      class="btn btn-success"
    />
  </form>

  <!-- afficher le nombre de Tache + supprimer toute les tâches  -->
  <p>{{ task }}</p>
  <option-task :taskList1="taskList" v-if="taskList.length >= 1"></option-task>
  <!-- Afficher la liste de tâches -->

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
import { ref } from "@vue/reactivity";
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
  setup(props) {
    const task = ref(0);
    task.value = props.index;
    console.log(task);
    return { task };
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

<style>
.btn-success {
  margin: 2vh;
}
</style>
