<template lang="html">
  <ul>
    <li>{{ student.name }}</li>
  </ul>
</template>

<script>
import { eventBus } from "../main.js";

export default {
  name: "students-favourite-list-item",
  props: ["student"]
}
</script>

<style lang="css" scoped>
li {
  display: inline;
  font: 13px Futura;
  padding-right: 10px;
}

button {
  padding: 10px;
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
