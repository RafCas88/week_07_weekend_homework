<template lang="html">
  <h2>{{ title }}</h2>
</template>

<script>
export default {
  name: "student-header",
  props:["title"]
};
</script>

<style lang="css" scoped>
h2 {
  font: bold 30px Futura;
  color: white;
  background-color: black;
  padding: 5px;
}
</style>
