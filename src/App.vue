<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" class="logo">
    <ScoreBoard msg="Vue ScoreBoard"/>
  </div>
</template>

<script>
import ScoreBoard from './components/ScoreBoard.vue'
import ScoreCounter from './components/ScoreCounter.vue'
export default {
  name: 'app',
  components: {
    ScoreBoard,
    ScoreCounter
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background-color: rgb(236, 243, 238);
}
.logo {
  animation: logo-spin infinite 20s linear;
  height: 150px;
}
@keyframes logo-spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}
</style>