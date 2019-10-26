<template lang="html">
  <div class="studentslistitem">
    <ul>
      <li>{{ student.name }}</li>
    </ul>
    <button @click="handleClick">Add to Favourites</button>
  </div>
</template>

<script>
import { eventBus } from "../main.js";

export default {
  name: "students-list-item",
  props:["student"],
  methods: {
    handleClick() {
      eventBus.$emit("favourite-added", this.student);
    }
  }
};
</script>

<style lang="css" scoped>
</style>
