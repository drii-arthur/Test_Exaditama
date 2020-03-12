<template>
  <div id="app">
    <Header/>
    <div class="container">
      <div class="add-filter">
        <AddTodo/>
        <span style="margin-bottom:auto;margin-top:auto">Filter Todos</span>
        <FilterTodo/>
      </div>
      <Todos/>
    </div>
  </div>
</template>

<script>
import Todos from "./components/Todos.vue";
import Header from "./components/Header.vue";
import AddTodo from "./components/AddTodo";
import FilterTodo from "./components/FilterTodo";
export default {
  name: "App",
  components: {
    Todos,
    Header,
    AddTodo,
    FilterTodo
  }
};
</script>

<style scoped>
body {
  line-height: 1.6;
  margin: 0;
}
.container {
  max-width: 1200px;
  box-sizing: border-box;
  margin: auto;
}
span {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  font-weight: 700;
  margin-right: 5px;
}
.add-filter {
  display: flex;
  padding: 20px 0px;
}
</style>
