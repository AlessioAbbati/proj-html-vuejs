<script>
export default {
    props: {
        football: Object,
    },
    data() {
        return {
            expanded: false,
        }
    },
    methods: {
        expandCard() {
            this.expanded = !this.expanded;
        }, 
    }
}
</script>

<template>
  <div class="card d-flex flex-column" :class="{ 'expanded': expanded }">
    <div class="img d-flex flex-column align-items-center">
        <img :src="football.img" :alt="football.title">
        <small>{{ football.date }} - Football</small>
    </div>
    <div class="info d-flex flex-column align-items-center">
        <h2>{{ football.title }}</h2>
        <small>{{ football.description }}</small>
        <button @click="expandCard">More</button>
    </div>
  </div>

</template>

<style lang="scss" scoped>
.card {
    width: calc(100% / 4);
    margin-inline: .5rem;
    margin-bottom: 5rem;
    -webkit-box-shadow: 0px 0px 19px 0px rgba(0,0,0,0.83);
    -moz-box-shadow: 0px 0px 19px 0px rgba(0,0,0,0.83);
    box-shadow: 0px 0px 19px 0px rgba(0,0,0,0.83);
    &.expanded {
        width: 50%;
        margin-inline: 0;
        margin-bottom: 5rem;
        transition: all 0.3s ease-in-out;
    }
    @media (max-width: 768px) {
        width: calc(100% / 2);
        &.expanded {
            width: 70%;
        }
    }
    img {
        width: 70%;
        margin-top: 1rem;
    }
    .info {
        small {
            padding-inline: 2rem;
        }
        button {
            background-color: black;
            color: white;
            padding: .8rem 2.5rem;
            border-radius: 1.3rem;
            margin-top: 1rem;
            margin-bottom: 1rem;
        }
    }
}
</style>
