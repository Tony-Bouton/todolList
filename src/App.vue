<template>
  <h1>Ma to-do list VueJs</h1>
  <div class="container">
    <CreateTask></CreateTask>
  </div>
</template>

<script>
import CreateTask from "./components/CreateTask.vue";
export default {
  name: "App",
  components: { CreateTask },
};
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

.container {
  margin-left: auto;
  margin-right: auto;
  border-radius: 10px;
  width: 50vw;
  padding: 10vw;
}
</style>
