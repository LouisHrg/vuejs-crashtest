<template>
   <li>
    {{ fullname }} : {{ student.color }}
  </li>
</template>

<script>
  export default {
    props: {
      student: { type: Object, required: true }
    },
    computed: {
      fullname() {
        return `${this.student.name} ${this.student.lastname}`
      }
    }
  }
</script>
