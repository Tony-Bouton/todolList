<template>
  <li>
    {{ todo }} <button @click="taskList1.splice(index, 1)">supprimer</button>
  </li>
</template>

<script>
export default {
  props: ["todo", "index", "taskList1"],

  methods: {},
};
</script>

<style></style>
