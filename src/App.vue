<script>
export default {
  name: "App",

  data() {
    return {

      todolist: [
        {
          text: "Ascoltare la registrazione Boolean del 23/01/24",
          done: true,
        },
        {
          text: "Fare esercizio Boolean del 23/01/24",
          done: false,
        },
        {
          text: "Fare il bucato",
          done: false,
        },
        {
          text: "Archiviare ricevute",
          done: false,
        },
        {
          text: "Fare esercizio di calligrafia",
          done: true,
        }
      ]
    };
  }

};
</script>


<template>
  <ul>
    <li v-for="todo in todolist">
      <span :class="{ line: todo.done }">{{ todo.text }}</span>

    </li>
  </ul>
</template>


<style>
.line {
  text-decoration: line-through;
}
</style>

