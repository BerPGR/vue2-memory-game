<template>
  <div class="card-container">
    <img :src="carta.img" alt="">
  </div>
</template>

<script>
export default {
    name: 'CardComponent',
    props: {
        carta: Object
    },
}
</script>

<style scoped>
    .card-container {
        height: 200px;
        width: 125px;
        border-radius: 25px;
        display: flex;
        align-items: center;
        justify-content: center;
        border: 2px solid black;
        background-color: aqua;
    }

    img {
        width: 100%;
        height: 100%;
        object-fit: contain;
    }
</style>