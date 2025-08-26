<template>
  <div id="app">
    <Greeting username="John" />
    <Students />
  </div>
</template>

<script>
import Greeting from './components/Greeting.vue';
import Students from './components/Students.vue';

export default {
  name: 'App',
  components: {
    Greeting,
    Students
  }
}
</script>
