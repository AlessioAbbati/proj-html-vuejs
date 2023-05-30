<script>
import AppMatches from "./AppMatches.vue"
import AppCards from "./AppCards.vue"
import AppRank from './AppRank.vue';
import AppResults from './AppResults.vue';


export default {
    components: { 
        AppMatches,
        AppCards,
        AppRank,
        AppResults,
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
            results: [
                {
                    team1: 'Instanbul Sports',
                    logo1: 'src/assets/img/league-club-1.png',
                    team2: 'United Fs Club',
                    logo2: 'src/assets/img/league-club-2.png',
                },
                {
                    team1: 'Schalke Club',
                    logo1: 'src/assets/img/league-club-3.png',
                    team2: 'Inter Club',
                    logo2: 'src/assets/img/league-club-4.png',
                },
                {
                    team1: 'Madrid Club',
                    logo1: 'src/assets/img/league-club-5.png',
                    team2: 'Borussia Club',
                    logo2: 'src/assets/img/league-club-6.png',
                },
                {
                    team1: 'Arsenal Club',
                    logo1: 'src/assets/img/league-club-7.png',
                    team2: 'Bayern Club',
                    logo2: 'src/assets/img/league-club-8.png',
                },
                {
                    team1: 'Atletico Club',
                    logo1: 'src/assets/img/league-club-9.png',
                    team2: 'Instanbul Sports',
                    logo2: 'src/assets/img/league-club-1.png',
                },
                {
                    team1: 'United Fs Club',
                    logo1: 'src/assets/img/league-club-2.png',
                    team2: 'Schalke Club',
                    logo2: 'src/assets/img/league-club-3.png',
                },
                {
                    team1: 'Inter Club',
                    logo1: 'src/assets/img/league-club-4.png',
                    team2: 'Madrid Club',
                    logo2: 'src/assets/img/league-club-5.png',
                },
                {
                    team1: 'Borussia Club',
                    logo1: 'src/assets/img/league-club-6.png',
                    team2: 'Arsenal Club',
                    logo2: 'src/assets/img/league-club-7.png',
                },
                {
                    team1: 'Bayern Club',
                    logo1: 'src/assets/img/league-club-8.png',
                    team2: 'Atletico Club',
                    logo2: 'src/assets/img/league-club-9.png',
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
  <section class="rankings d-flex justify-content-around">
    <div class="rank">
       <app-rank />
    </div>
    <div class="results">
       <app-results 
            v-for="result in this.results" 
            :key="result"
            :info="result"
       />
    </div>
  </section>
  <div class="bet">
    <img class="img-fluid" src="../assets/img/reklam.jpg" alt="">
  </div>
</template>

<style lang="scss" scoped>
.cards {
    background-image: url('../assets/img/player.jpg');
    h3 {
        color: white;
        margin-top: 2rem;
        margin-bottom: 3rem;
    }
    .card {
        background-color: transparent;
        padding-inline: 1rem;
        border-radius: 2rem;
    }
    button {
        color: white;
        background-color: black;
        border: 1px solid white;
        border-radius: 3rem;
        padding: .6rem;
        margin-top: 2rem;
        margin-bottom: 2rem;
    }
}
.bet {
    width: 100%;
}
</style>
