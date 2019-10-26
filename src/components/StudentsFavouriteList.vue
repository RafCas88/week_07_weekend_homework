<template lang="html">
  <div id="favourite-list">
    <student-header title="Your Favourites"></student-header>
    <ul>
      <students-favourite-list-item v-for="(student, index) in favourite"
      :student="student" :key="index"></students-favourite-list-item>
    </ul>
  </div>
</template>

<script>
import StudentsFavouriteListItem from "../components/StudentsFavouriteListItem.vue";
import StudentHeader from "../components/StudentHeader.vue";

export default {
  name: "students-favourite-list",
  props:["favourite"],
  components: {
    "students-favourite-list-item": StudentsFavouriteListItem,
    "student-header": StudentHeader
  }
};
</script>

<style lang="css" scoped>
</style>
