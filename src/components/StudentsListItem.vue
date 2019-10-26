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

li {
  font: bold 13px Futura;
}

.studentlistitem {
  display: flex;
  flex-direction: column;
  padding: 20px;
  align-items: center;
  width: 150px;
  height: 225px;
  border-radius: 25px;
  border: 2px solid dodgerblue;
  background-color: white;
}

button {
  font: bold 11px Futura;
  text-decoration: none;
  background-color: #EEEEEE;
  color: #333333;
  padding: 2px 6px 2px 6px;
  border-top: 1px solid #CCCCCC;
  border-right: 1px solid #333333;
  border-bottom: 1px solid #333333;
  border-left: 1px solid #CCCCCC;
}
</style>
