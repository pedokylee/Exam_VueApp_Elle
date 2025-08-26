<template>
  <h1>YAWAAAAA</h1>
  <div>
    <ul v-if="showList">
      <li v-for="(student, index) in students" :key="index"
          :class="{ highlight: student.score >= 90 }">
        {{ student.name }} - {{ student.score }}
      </li>
    </ul>
    <p>Passing Students: {{ passingStudents }}</p>
  </div>
</template>

<script>
export default {
  name: 'StudentList',
  data() {
    return {
      showList: true,
      students: [
        { name: 'Megs', score: 85 },
        { name: 'Euns', score: 65 },
        { name: 'Mayang', score: 90 }
      ]
    }
  },
  computed: {
    passingStudents() {
      return this.students.filter(student => student.score > 70).length;
    }
  }
}
</script>

<style scoped>
.highlight {
  color: green;
  font-weight: bold;
}
</style>
