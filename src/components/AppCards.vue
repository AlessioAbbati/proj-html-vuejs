<script>
export default {
    props: {
        card: Object,
    }
}
</script>

<template>
  <div class="card d-flex justify-content-center align-items-center">
    <img :src="card.img" :alt="card.name">
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
    .info {
    background-color: black;
    border-radius: 1rem;
    padding: 0 1rem;
    span {
        color: white;
    }
}
}
</style>
