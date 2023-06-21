<template>
  <div id="app">
    <Card :carta="cartas[2]"/>
  </div>
</template>

<script>
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  },
  data: () => ({
    cartas: [
      {value: 0, img: require('@/assets/apple.png'), name: 'Apple'},
      {value: 1, img: require('@/assets/bananas.png'), name: 'Banana'},
      {value: 2, img: require('@/assets/eggplant.png'), name: 'Eggplant'},
      {value: 3, img: require('@/assets/grape.png'), name: 'Grape'},
      {value: 4, img: require('@/assets/lemon.png'), name: 'Lemon'},
      {value: 5, img: require('@/assets/orange.png'), name: 'Orange'},
      {value: 6, img: require('@/assets/pear.png'), name: 'Pear'},
      {value: 7, img: require('@/assets/watermelon.png'), name: 'Watermelon'},
    ]
  }),
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
