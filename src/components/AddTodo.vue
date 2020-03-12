<template>
  <div class="add">
    <button
      type="button"
      class="btn btn-secondary"
      data-toggle="modal"
      data-target="#staticBackdrop"
    >Add Todos</button>

    <!-- Modal -->
    <div
      class="modal fade"
      id="staticBackdrop"
      data-backdrop="static"
      tabindex="-1"
      role="dialog"
      aria-labelledby="staticBackdropLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="staticBackdropLabel">Add Todo</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>

          <form @submit="onSubmit">
            <div class="modal-body">
              <input type="text" v-model="title" placeholder="Insert Todo" class="name">
            </div>
            <div class="modal-footer">
              <button type="button" class="btn btn-danger" data-dismiss="modal">Close</button>
              <input type="submit" value="Submit" class="btn btn-secondary">
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapActions } from "vuex";
export default {
  name: "AddTodo",
  data() {
    return {
      title: ""
    };
  },
  methods: {
    ...mapActions(["addTodo"]),
    onSubmit(e) {
      e.preventDefault();
      this.addTodo(this.title);
      this.title = "";
    }
  }
};
</script>

<style>
.add {
  margin-right: 20px;
}
.btnn {
  background-color: #222f3e;
  color: blanchedalmond;
}
.name {
  width: 100%;
  border-radius: 5px;
  padding: 5px 10px;
}
</style>