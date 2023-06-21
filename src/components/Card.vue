<template>
  <div class="card-container" @click="showCartas" :style="{backgroundImage: 'url('+carta.img+')'}"></div>
</template>

<script>

export default {
    name: 'CardComponent',
    props: {
        carta: Object
    },
    methods: {
        showCartas () {
            console.log(this.carta.img);
        }
    }
}
</script>

<style>
    .card-container {
        height: 200px;
        width: 100px;
        border: 1px solid black;
    }
</style>