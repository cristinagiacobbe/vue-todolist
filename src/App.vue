<script>
export default {
  name: "App",

  data() {
    return {
      todolist: [
        {
          text: "learn HTML",
          done: true,
        },
        {
          text: "learn CSS",
          done: true,
        },
        {
          text: "learn Javascript",
          done: true,
        },
      ],
      userTodo: [
        {
          text: "",
          done: true,
        }
      ],
      finalTodo: []
    }
  },
  methods: {
    removeTodo(i) {
      this.todolist.splice(i, 1);
    },
    addTodo() {
      this.todolist.text = this.userTodo.text
      this.todolist.done = this.userTodo.done
      console.log(this.todolist);
    },
  }
}
</script>


<template>
  <div class="container">
    <div class="card">
      <div class="card-body">
        <h1>Todolist</h1>

        <div class="input-group mb-3">
          <input type="text" v-model="userTodo.text" @keyup.enter="addTodo" class="form-control"
            placeholder="Aggiungi una voce alla lista">
          <button @click="addTodo" class="btn btn-outline-secondary" type="button" id="button-addon2">Aggiungi</button>
        </div>

        <ul v-if="todolist.length > 0">

          <li v-for="( todo, index ) in  todolist ">
            <span v-on:click="removeTodo(index)"> x </span>
            <span :class="{ line: todo.done }" @click="todo.done = !todo.done">{{ todo.text }}</span>
          </li>
        </ul>
        <p v-else>
          ✌️Nothing to show !! ✌️
        </p>
      </div>
    </div>
  </div>
</template>


<style>
.line {
  text-decoration: line-through;
}
</style>

