<script>
export default {
    props: {
        card: Object,
    }
}
</script>

<template>
  <div class="card d-flex justify-content-center align-items-center">
    <div class="img">
        <img :src="card.img" :alt="card.name">
    </div>
    <div class="info d-flex flex-column justify-content-center align-items-center">
        <span>{{ card.number }}</span>
        <span>{{ card.name }}</span>
        <span>{{ card.role }}</span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
    background-color: black;
    .img {
        width: 100%;
        img {
            width: 100%;
            border-radius: 2rem;
        }
    }
    .info {
    background-color: black;
    border-radius: 1rem;
    width: 100%;
    span {
        color: white;
    }
}
}
</style>
