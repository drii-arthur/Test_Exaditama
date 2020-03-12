<template>
  <select @change="filterTodos($event)">
    <option value="10">10</option>
    <option value="20">20</option>
    <option value="50">50</option>
    <option value="100">100</option>
    <option value="200">200</option>
  </select>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "FilterTodo",
  methods: mapActions(["filterTodos"])
};
</script>

<style>
select {
  border-radius: 5px;
  padding: 2px 7px;
}
</style>