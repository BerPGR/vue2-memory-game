<template>
  <div :class="{'card-container': toogleCarta === true, 'card-none': toogleCarta === false}" @click="showCard">
    <img v-if="toogleCarta===true" :src="carta.img" alt="">
  </div>
</template>

<script>
export default {
    name: 'CardComponent',
    props: {
        carta: Object
    },
    data: () => ({
        toogleCarta: false
    }),
    methods: {
        showCard () {
            this.toogleCarta = !this.toogleCarta
        }
    }
}
</script>

<style scoped>
    .card-container {
        margin: 20px;
        height: 150px;
        width: 100px;
        border-radius: 25px;
        display: flex;
        align-items: center;
        justify-content: center;
        border: 2px solid black;
        background-color: aqua;
    }

    .card-none {
        margin: 20px;
        height: 150px;
        width: 100px;
        border-radius: 25px;
        border: 2px solid black;
        background-color: blue;
    }

    img {
        width: 100%;
        height: 100%;
        object-fit: contain;
    }
</style>