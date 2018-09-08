<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Jeff Webb
    </p>
    <div class="teams">
      <ScoreCounter />
      <ScoreCounter />
    </div>
  </div>
</template>

<script>
import ScoreCounter from './ScoreCounter.vue'
export default {
  name: 'Scoreboard',
  components: {
    ScoreCounter
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
a {
  color: #002868;
}
.teams {
  display: flex;
  justify-content: space-around;
}
</style>
