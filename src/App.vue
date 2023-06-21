<template>
  <div id="app">
    <div class="memory-container">
      <Card v-for="(card, i) in cartas" :key="i" :carta="card"/>
    </div>
  </div>
</template>

<script>
import Card from './components/Card.vue'
import cards from './model/cards'
export default {
  name: 'App',
  components: {
    Card
  },
  data: () => ({
    cartas: []
  }),
  mounted() {
    this.createMemoryArray(0)
  },
  methods: {
    createMemoryArray (index) {
      let repeat = 0;
      for (index; index<(cards.length * 2); index++) {
        let randomCard = Math.floor(Math.random() * 8)
        for (let j = 0; j <(cards.length *2); j++) {
          if (cards[randomCard] == this.cartas[j]) {
            repeat++;
          }
        }

        if (repeat == 0) {
          this.cartas.push(cards[randomCard])
        }
        if (repeat == 1) {
          this.cartas.push(cards[randomCard])
          repeat = 0
        }
        if (repeat >= 2) {
          this.createMemoryArray(index)
        }
      }
    }
  }
  /*
  mounted() {
    let repeat = 0;
    for (let i = 0; i<(cards.length * 2); i++) {
      let randomNumber = Math.floor(Math.random() * 8)
      
      for(let j = 0; j<(cards.length * 2); j++) {
        if (cards[randomNumber] == this.cartas[j])
      }
      if (repeat == 0) {
        this.cartas[i] = cards[randomNumber]
      }
      if (repeat == 1) {
        this.cartas[i] = cards[randomNumber]
        repeat = 0
      }
    }
  }
  */
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

.memory-container {
  display: flex;
  justify-content: center;
  padding: 0 80px;
  flex-wrap: wrap;
}
</style>
