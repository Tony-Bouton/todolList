<template>
  <li>
    <div class="wrapper1">
      <span class="todo"> {{ todo }} </span>
      <label for="done"
        >Terminée <input type="checkbox" name="done" id="done" /></label
      ><button @click="taskList1.splice(index, 1)" class="btn btn-danger">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="16"
          height="16"
          fill="currentColor"
          class="bi bi-trash"
          viewBox="0 0 16 16"
        >
          <path
            d="M5.5 5.5A.5.5 0 0 1 6 6v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5zm2.5 0a.5.5 0 0 1 .5.5v6a.5.5 0 0 1-1 0V6a.5.5 0 0 1 .5-.5zm3 .5a.5.5 0 0 0-1 0v6a.5.5 0 0 0 1 0V6z"
          />
          <path
            fill-rule="evenodd"
            d="M14.5 3a1 1 0 0 1-1 1H13v9a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V4h-.5a1 1 0 0 1-1-1V2a1 1 0 0 1 1-1H6a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1h3.5a1 1 0 0 1 1 1v1zM4.118 4 4 4.059V13a1 1 0 0 0 1 1h6a1 1 0 0 0 1-1V4.059L11.882 4H4.118zM2.5 3V2h11v1h-11z"
          />
        </svg>
      </button>
    </div>
  </li>
</template>

<script>
export default {
  props: ["todo", "index", "taskList1"],

  methods: {},
};
</script>

<style>
.wrapper1 {
  display: flex;
  justify-content: center;
  border: rgb(163, 161, 161) solid 0.8px;
  margin-left: auto;
  margin-right: auto;
  border-radius: 10px;

  padding: 10%;
}
li {
  list-style: none;
  display: flex;
  justify-content: space-around;
  margin: 2%;
}
.todo {
  margin-right: 20%;
}
</style>
