<template lang="html">
  <img :src="checkForImage"/>
  <li>{{ harryPotter.image }}</li>
</template>

<script>
export default {
  name: "students-image",
  props:["imageUrl"],
  computed: {
    checkForImage(){
      return this.imageUrl != undefined ? this.imageUrl : noImage;
    }
  }
}
</script>

<style lang="css" scoped>
</style>
