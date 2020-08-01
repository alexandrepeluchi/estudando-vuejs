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
        <tr>
          <td>1</td>
          <td>Jack</td>
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
      this.students.push(this.name);
      this.students.forEach((element) => {
        console.log(element);
      });
    },
  },
};
</script>

<style scoped>
</style>
