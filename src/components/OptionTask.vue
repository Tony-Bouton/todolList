<template>
  <p>
    nombre de taches : {{ taskList1.length }}
    <button @click="taskList1.length = null">suppprimer toutes</button>
  </p>
</template>

<script>
export default {
  props: ["taskList1"],
};
</script>

<style></style>
