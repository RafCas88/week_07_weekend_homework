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
</style>
