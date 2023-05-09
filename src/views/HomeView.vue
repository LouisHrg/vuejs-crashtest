<template>
  <main>
    <p @click="toggleList"> Toggle student list </p>

    <StudentList v-if="isVisible" :students="students"/>

    <label>
      Mon input
      <input type="text" v-model="form.input"/>
    </label>
    <br>
    <br>
    <label>
      Mon password
      <input type="password" v-model="form.password"/>
    </label>
    <br>
    <br>
    <button @click="submitForm"> Sauvegarder </button>
  </main>
</template>


<script>
  import StudentList from '@/components/StudentList.vue'

  export default {
    components: {
      StudentList,
    },
    data() {
      return {
        students: [
          { name: 'toto', lastname: "qzod", color: 'red'},
          { name: 'tata', lastname: "qzldlld",  color: 'blue'},
          { name: 'prout', lastname: "kqzd",  color: 'yellow'},
          { name: 'ntm', lastname: "Aaaaaa",  color: 'green'},
        ],
        color: true,
        isVisible: false,
        form : {
          input: null,
          password: null,
        },
      };
    },
    methods: {
      toggleList() {
        this.isVisible = !this.isVisible
      },
      submitForm() {
        console.log(this.form);
      }
    }
  }
</script>
