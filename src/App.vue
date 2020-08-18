<template>
  <div id="app">
    
    <HeroGames/>
  </div>
</template>

<script>

import HeroGames from './components/HeroGames.vue'

export default {
  name: 'App',
  components: {
    HeroGames,
  }
    
    
  
    
  
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
