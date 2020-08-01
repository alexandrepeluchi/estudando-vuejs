<template>
  <div>
    <h1>{{title}}</h1>
    <input type="text" placeholder="Student name" v-model="name" v-on:keyup.enter="addStudent()" />
    <table border="1px">
      <thead>
        <th>Registration</th>
        <th>Name</th>
        <th>Options</th>
      </thead>
      <tbody>
        <tr v-for="(student, index) in students" :key="index">
          <td>{{index+1}}</td>
          <td>{{student.name}}</td>
          <td>
            <button class="btn" @click="remove()">Remove</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "Student",
      name: "tete",
      students: [],
    };
  },
  props: {},
  methods: {
    addStudent() {
      let _student = {
        name: this.name,
      };
      this.students.push(_student);
      this.name = "";
    },
  },
};
</script>

<style scoped>
</style>
