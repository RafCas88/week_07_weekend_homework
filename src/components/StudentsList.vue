<template lang="html">
  <div >
    <students-list-item v-for="(student, index) in students"
    :student="student" :key="index"></students-list-item>
  </div>
</template>

<script>
import StudentsListItem from "../components/StudentsListItem.vue";

export default {
  name: "students-list",
  props: ["students"],
  components: {
    "students-list-item": StudentsListItem
  }
};
</script>
<style lang="css" scoped>
</style>
