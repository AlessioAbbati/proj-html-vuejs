<script>
import AppMatches from "./AppMatches.vue"
import AppCards from "./AppCards.vue"


export default {
    components: { 
        AppMatches,
        AppCards,
    },
    data() {
        return {
            cards: [
                {
                    img: 'src/assets/img/player1.jpg',
                    number: '07',
                    name: 'Adam Brown',
                    role: 'Forwarder',
                },
                {
                    img: 'src/assets/img/player2.jpg',
                    number: '09',
                    name: 'Michael Kayn',
                    role: 'Forwarder',
                },
                {
                    img: 'src/assets/img/player3.jpg',
                    number: '11',
                    name: 'Michael Lee',
                    role: 'Forwarder',
                },
                {
                    img: 'src/assets/img/player4.jpg',
                    number: '15',
                    name: 'Ethan Smith',
                    role: 'Midfielder',
                },
            ],
        }
    },
};
</script>

<template>
  <section class="sec_carousel">
    <app-matches />
  </section>
  <section class="cards d-flex flex-column align-items-center">
    <h3>Players</h3>
    <div class="card d-flex flex-row">
        <app-cards 
            v-for="player in this.cards" 
            :key="player.name"
            :card="player"
        />
    </div>
    <button><small>View All Players</small></button>
  </section>
</template>

<style lang="scss" scoped>
.cards {
    background-image: url('../assets/img/player.jpg');
    h3 {
        color: white;
    }
    .card {
        gap: 10rem;
        background-color: transparent;
        padding-top: 1rem;
        padding-bottom: 1rem;
    }
    button {
        color: white;
        background-color: black;
        border: 1px solid white;
        border-radius: 3rem;
        padding: .6rem;
    }
}
</style>
