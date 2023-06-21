<template>
  <div id="app">
    <Card :carta="cartas[1]"/>
  </div>
</template>

<script>
import Card from './components/Card.vue'
import cards from './models/cards.js'

export default {
  name: 'App',
  components: {
    Card
  },
  data: () => ({
    cartas: []
  }),
  mounted() {
    for (let carta of cards) {
      this.cartas = [...this.cartas, carta]
    }
  },
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

#app {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
</style>
