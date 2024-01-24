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
    }
  }
}
</script>

<template>
  <h1>My todolist</h1>
  <ul>
    <li v-for="action in todolist">
      {{ action.text }}
    </li>
  </ul>
</template>

<style></style>
