<template>
  <p>{{ capitalizedMessage }}</p>
</template>

<script>
import { capitalize } from '../utils.js';

export default {
  name: 'UserGreeting',
  props: {
    username: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      message: `hello, ${this.username}! welcome to the My Vue App.`
    }
  },
  computed: {
    capitalizedMessage() {
      return this.message.split(' ').map(word => capitalize(word)).join(' ');
    }
  }
}
</script>
