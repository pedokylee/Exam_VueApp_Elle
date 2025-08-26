<template>
  <section>
    <h2>Greeting Component</h2>

    <p>{{ capitalizedMessage }}</p>

    <p>Hello, {{ username }}</p>
  </section>
</template>

<script>
import { capitalize } from "../utils.js";

export default {
  name: "GreetingComponent",
  props: {
    username: { type: String, required: true },
  },
  data() {
    return {
      message: "hello from greeting component",
    };
  },
  computed: {
    capitalizedMessage() {
      return capitalize(this.message);
    },
  },
};
</script>
