<template>
  <img alt="Vue logo" src="./assets/">
</template>

<script>
export default {
  name: 'App',
  components: {
    
    
  },
  randomDamage: function(min, max) {             
    return Math.max(Math.floor(Math.random() * max) + 1, min);    
    },
    
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
