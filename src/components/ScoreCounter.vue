<template>
  <div class="teamScore">
    <h3>{{teamDisplayName}}</h3>
    <p>{{teamDisplayScore}}</p>
    <form v-on:submit.prevent="updateName">
      <input class="updateTeamName" placeholder="Update Name" v-model="teamName">

    </form>
    <div class="">
      <button class="updateScore" v-on:click="addOne">Add 1</button>
      <button class="updateScore" v-on:click="subtractOne">Subtract 1</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ScoreCounter",
  props: {
    team: String
  },
  data: function() {
    return {
      teamName: "",
      teamDisplayName: "Team",
      teamDisplayScore: 0
    };
  },
  methods: {
    updateName: function() {
      this.teamDisplayName = this.teamName;
      this.teamName = ""
    },
    addOne: function() {
      this.teamDisplayScore++;
    },
    subtractOne: function() {
      if (this.teamDisplayScore > 0) {
        this.teamDisplayScore--;
      }
    }
  }
};
</script>

<style scoped>
.teamScore {
  margin: 3em;
  padding: 5em;
  border: 1px solid black;
  border-radius: 10px;
  background-color:   rgb(236, 241, 243);
}
.updateTeamName {
  font-size: 20px;
  text-align: center;
}
.updateScore {
  font-size: 1.5em;
}
</style>