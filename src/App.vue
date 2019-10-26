<template lang="html">
  <div id="app">
    <student-header title="Hogwarts Students"/>
    <student-header v-if="!harryPotter.length" title="LOADING..." />
    <students-list :students="harryPotter"></students-list>
    <students-favourite-list :favourite="favouriteStudents"></students-favourite-list>
  </div>
</template>

<script>
import { eventBus } from "./main.js";
import StudentsList from "./components/StudentsList.vue";
import StudentHeader from "./components/StudentHeader.vue";
import StudentsFavouriteList from "./components/StudentsFavouriteList.vue";

export default {
  name: "app",
  data(){
    return {
      harryPotter: [],
      favouriteStudents: []
    }
  },
  computed: {
    favourite() {
      favouriteStudents = student.isFavourite
      return this.students.filter(student => student.isFavourite);

    }
  },
  mounted (){
    fetch("http://hp-api.herokuapp.com/api/characters")
    .then(response => response.json())
    .then(harryPotterData => this.harryPotter= harryPotterData)

    eventBus.$on("favourite-added", student => this.favouriteStudents.push(student));
  },
  components: {
    "student-header": StudentHeader,
    "students-list": StudentsList,
    "students-favourite-list": StudentsFavouriteList
  }
}
</script>

<style lang="css" scoped>
#app {
  background-color: #6EC3F4;
}

#list-info {
  display: flex;
}
</style>
