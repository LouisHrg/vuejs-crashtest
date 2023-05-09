<template>
  <ul>
    <StudentItem
      v-for="student in students"
      :key="student.name"
      :student="student"
      />
  </ul>
</template>

<script>
  import StudentItem from '@/components/StudentItem.vue'
  export default {
    components: {
      StudentItem,
    },
    props: {
      students: { type: Array, required: true },
    },
  }
</script>
