<template lang="html">

  <div id="main-container">

    <h1>Tour de France 2020</h1>
    <h3>coverage from The Guardian</h3>
    



  </div>
  
</template>

<script>
export default {
  name: "app",

  data() {
    return {
      TdfCoverage: []
    }
  },

mounted() {
  fetch("https://content.guardianapis.com/search?section=sport&from-date=2020-08-29&to-date=2020-09-20&order-by=oldest&page-size=200&q=tour%20de%20france%202020&api-key=test")
  .then(res => res.json())
  .then(TdfCoverageAPI => this.TdfCoverage = TdfCoverageAPI.response.results)
},

};
</script>

<style lang="css" scoped>

</style>