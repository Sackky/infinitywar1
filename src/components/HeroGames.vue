<template>
<div>
    <div id="random">
      <button @click="Arandom()">Attack</button>
      <button @click="ASPrandom()">Special Attack</button>
      <p v-bind:style="{}"></p>
      <HeroGames/>
      <br>
      Player HP {{playerHP}}
      <br>
      Monster HP {{monsterHP}}
      <br>
      <div v-if="monsterHP <= 0">
      <h1>Player Win</h1>
      </div>
      <div v-if="playerHP <= 0">
      <h1>Monster Win</h1>
      </div>
    </div>
</div>
    
</template>

<script>
export default {
    data: function () {
    return {
      playerpower: '',
      monsterpower: '',
      playerHP: 100,
      monsterHP: 100,
    };
  },
    methods:{
      Arandom: function() {
      this.playerpower = Math.floor(Math.random() * 7 + 3);
      this.monsterHP = this.monsterHP - this.playerpower;
      this.monsterpower = Math.floor(Math.random() * 7 + 3);
      this.playerHP = this.playerHP - this.monsterpower;
      },
      ASPrandom: function() {
      this.playerpower = Math.floor(Math.random() * 10 + 5);
      this.monsterHP = this.monsterHP - this.playerpower;
      this.monsterpower = Math.floor(Math.random() * 10 + 5);
      this.playerHP = this.playerHP - this.monsterpower;
      }
    }
}
</script>

<style>

</style>