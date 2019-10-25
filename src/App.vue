<template lang="html">

</template>

<script>
export default {
  name: "app",
  data(){
    return {
      harryPotterData: []
    }
  },
  mounted (){
    fetch("http://hp-api.herokuapp.com/api/characters")
    .then(response => response.json())
    .then(harryPotterData => this.harryPotterData = harryPotterData)
  },
}
</script>

<style lang="css" scoped>
</style>
