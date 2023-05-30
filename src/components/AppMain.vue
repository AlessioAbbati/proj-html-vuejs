<script>
import AppMatches from "./AppMatches.vue"
import AppCards from "./AppCards.vue"
import AppRank from './AppRank.vue';
import AppResults from './AppResults.vue';
import AppSponsor from './AppSponsor.vue';
import AppRules from './AppRules.vue';
import AppMatchDay from './AppMatchDay.vue';


export default {
    components: { 
        AppMatches,
        AppCards,
        AppRank,
        AppResults,
        AppSponsor,
        AppRules,
        AppMatchDay,
    },
    data() {
        return {
            matchDay: [
                {
                    team1: 'Instanbul Sports',
                    logo1: 'src/assets/img/club-1.png',
                    team2: 'United Fs Club',
                    logo2: 'src/assets/img/club-2.png',
                    date: 'May 21, 2022 18.05 pm',
                    stadium: 'Expert Stadium',
                },
            ],
            matches: [
                {
                    team1: 'Schalke Club',
                    logo1: 'src/assets/img/club-3.png',
                    team2: 'Inter Club',
                    logo2: 'src/assets/img/club-4.png',
                    date: 'October 20, 2022 17.00 pm',
                    stadium: 'Expert Stadium',
                },
                {
                    team1: 'Atletico Club',
                    logo1: 'src/assets/img/club-9.png',
                    team2: 'Borussia Club',
                    logo2: 'src/assets/img/club-6.png',
                    date: 'September 18, 2022 21.00 pm',
                    stadium: 'Expert Stadium',
                },
                {
                    team1: 'United Fs Club',
                    logo1: 'src/assets/img/club-2.png',
                    team2: 'Bayern Club',
                    logo2: 'src/assets/img/club-8.png',
                    date: 'August 3, 2022 19.00 pm',
                    stadium: 'Expert Stadium',
                },
                {
                    team1: 'Arsenal Club',
                    logo1: 'src/assets/img/club-7.png',
                    team2: 'Atletico Club',
                    logo2: 'src/assets/img/club-4.png',
                    date: 'July 8, 2022 12.00 pm',
                    stadium: 'Expert Stadium',
                },
                {
                    team1: 'Instanbul Sports',
                    logo1: 'src/assets/img/club-1.png',
                    team2: 'United Fs Club',
                    logo2: 'src/assets/img/club-2.png',
                    date: 'June 12, 2022 09.00 am',
                    stadium: 'Expert Stadium',
                },
            ],
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
            rules: [
                {
                    img: 'src/assets/img/news1-1.png',
                    date: '29/05/2022',
                    title: 'What is Football',
                    description: 'Football is a sport that is known as a ball game and is loved by [...]',
                },
                {
                    img: 'src/assets/img/news2-1.png',
                    date: '29/05/2022',
                    title: 'Football Rules',
                    description: 'GOLDEN GOAL: in a football match, the goal scored by one of the teams in [...]',
                },
                {
                    img: 'src/assets/img/news3-1.png',
                    date: '29/05/2022',
                    title: 'Football Features',
                    description: 'Football: it is an aerobic-based anaerobic sport in which jumps, kiks, turns, running with changing [...]',
                },
                {
                    img: 'src/assets/img/news4-1.png',
                    date: '29/05/2022',
                    title: 'Football Terms',
                    description: 'GOLDEN GOAL: in a football match, the goal scored by one of the teams in [...]',
                },
            ]
        }
    },
};
</script>

<template>
    <section class="matchDay">
        <div class="container">
            <app-match-day
                v-for="match in this.matchDay"
                :key="match"
                :matchDay="match"
            />
        </div>
    </section>
    <section class="matches">
        <div class="container">
            <h1 class="text-center text-light">Upcoming Matches</h1>
            <app-matches 
                v-for="match in this.matches" 
                :key="match" 
                :match="match" 
            />
        </div>
    </section>
    <section class="cards d-flex flex-column align-items-center">
        <h3>Players</h3>
        <div class="card d-flex flex-row">
            <app-cards v-for="player in this.cards" :key="player.name" :card="player" />
        </div>
        <button><small>View All Players</small></button>
    </section>
    <section class="rankings d-flex justify-content-around">
        <div class="rank">
            <h2 class="text-center text-dark">League Table</h2>
            <app-rank />
            <button>View Full League Table</button>
        </div>
        <div class="results">
            <h2 class="text-center text-dark">Fixtures & Results</h2>
            <div class="container">
                <app-results v-for="result in this.results" :key="result" :info="result" />
            </div>
            <button>View Full Fixtures</button>
        </div>
    </section>
    <section class="bet">
        <img class="img-fluid" src="../assets/img/reklam.jpg" alt="">
    </section>
    <section class="sponsor d-flex align-items-center justify-content-around">
        <app-sponsor />
    </section>
    <section class="rules d-flex flex-column align-items-center">
        <div>
            <div class="logo d-flex flex-column align-items-center">
                <img src="../assets/img/OIP.jpg" alt="">
                <h2>Results & new articles</h2>
                <small>Be aware of the football world</small>
            </div>
        </div>
        <div class="d-flex">
            <app-rules v-for="rule in this.rules" :key="rule.title" :football="rule" />
        </div>
        <div class="buttons d-flex justify-content-center">
            <button></button>
            <button></button>
            <button></button>
            <button></button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.matchDay {
    margin-top: 1rem;
}
.matches {
    background-image: url('../assets/img/saha.jpg');
    background-size: cover;
    .container {
        h1 {
            padding-top: 2rem;
            margin-bottom: 2rem;
        }
    }
}
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

.rankings {
    h2 {
        margin: 2rem 0;
    }
    .container {
        & > :nth-child(odd) {
            background-color: #EBEBEB;
        }
        & > :nth-child(even) {
            background-color: #F3F3F3;
        }
    }
    button {
        width: 100%;
        padding: 1rem;
        background-color: black;
        color: white;
    }
}

.bet {
    width: 100%;
}

.sponsor {
    width: 100%;
    background-color: black;
    height: 12rem;
    padding-inline: 1rem;
}

.rules {
    .logo {
        width: 100%;
        margin-top: 3rem;
        margin-bottom: 2rem;

        img {
            width: 20%;
        }

        h2 {
            font-weight: 700;
        }
    }

    .buttons {
        margin-bottom: 3rem;

        button {
            padding: .2rem 1rem;
            margin-inline: .5rem;
            border-radius: 2rem;
            background-color: #EBEBEB;

            &:hover {
                background-color: black;
            }
        }
    }
}</style>
