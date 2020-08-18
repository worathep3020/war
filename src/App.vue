<template>
 <div id="app">
   
    <img alt="Vue logo" src="./assets/vs.png" width="300">
    <HelloWorld msg="Apocalypse War"/>
    <div class="row">
      <div class="col-12"><game Start="Start" End="End"/>

      </div>
    </div>
   </div>
    
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import game from './components/game.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    game
    
  },
  
  randomDamage: function(min, max) {             
    return Math.max(Math.floor(Math.random() * max) + 1, min);    
    },
  data :function(){
    return{
    total:0
    }

  },
  methods:{
    sum(counterValue){
      this.total += counterValue

    },
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

