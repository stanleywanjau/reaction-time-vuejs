<template>
 <h1 class="text-green-800 font-bold"> stanley Result Timer</h1>
 <button @click="start" :disabled="isPlaying" class="bg-green-300 hover:bg-green-500 p-4 rounded-xl ">Play</button>
 <Block v-if="isPlaying" :delay="delay" @end="endGame"/>
 <Results v-if="showResults" :score="score"/>
</template>

<script>
import Block from './components/BlockView.vue'
import Results from './components/ResultView.vue'
export default {
  name: 'App',
  components: {
   Block,Results
  },
  data() {
    return {
      isPlaying: false,
      delay: null,
      score:null,
      showResults: false
    }
  },
  methods: {
    start() {
      this.delay = 2000 + Math.random()*5000
      this.isPlaying = true
      this.showResults = false
    },
    endGame(reactionTime) {
      this.score = reactionTime
      this.isPlaying = false
      this.showResults = true
    }
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
