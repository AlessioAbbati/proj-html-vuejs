<script>
export default {
    data() {
        return {
            rankings: [
                {
                    position: '1',
                    logo: 'src/assets/img/league-club-1.png',
                    team: 'Instanbul Sports',
                    wins: '18',
                    draws: '2',
                    lose: '0',
                },
                {
                    position: '2',
                    logo: 'src/assets/img/league-club-2.png',
                    team: 'United Fs Club',
                    wins: '14',
                    draws: '2',
                    lose: '1',
                },
                {
                    position: '3',
                    logo: 'src/assets/img/league-club-3.png',
                    team: 'Schalke Club',
                    wins: '13',
                    draws: '3',
                    lose: '0',
                },
                {
                    position: '4',
                    logo: 'src/assets/img/league-club-4.png',
                    team: 'Inter Club',
                    wins: '13',
                    draws: '2',
                    lose: '1',
                },
                {
                    position: '5',
                    logo: 'src/assets/img/league-club-5.png',
                    team: 'Madrid Club',
                    wins: '12',
                    draws: '1',
                    lose: '2',
                },
                {
                    position: '6',
                    logo: 'src/assets/img/league-club-6.png',
                    team: 'Borussia Club',
                    wins: '11',
                    draws: '0',
                    lose: '3',
                },
                {
                    position: '7',
                    logo: 'src/assets/img/league-club-7.png',
                    team: 'Arsenal Club',
                    wins: '10',
                    draws: '5',
                    lose: '0',
                },
                {
                    position: '8',
                    logo: 'src/assets/img/league-club-8.png',
                    team: 'Bayern Club',
                    wins: '10',
                    draws: '2',
                    lose: '2',
                },
                {
                    position: '9',
                    logo: 'src/assets/img/league-club-9.png',
                    team: 'Atletico Club',
                    wins: '9',
                    draws: '0',
                    lose: '4',
                },
            ],
        }
    },
    methods: {
        calculatePoints(team) {
        return ((parseInt(team.wins) * 3) + parseInt(team.draws));
        }
    },
}
</script>

<template>
    <table>
      <thead>
        <tr>
          <th colspan="3">team</th>
          <th>W</th>
          <th>D</th>
          <th>L</th>
          <th>PTS</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(team, index) in rankings" :key="team.position">
          <td>{{ index + 1 }}</td>
          <td>
            <img :src="team.logo">
          </td>
          <td>{{ team.team }}</td>
          <td>{{ team.wins }}</td>
          <td>{{ team.draws }}</td>
          <td>{{ team.lose }}</td>
          <td>{{ calculatePoints(team) }}</td>
        </tr>
      </tbody>
    </table>
</template>

<style lang="scss" scoped>
thead {
    background-color: black;
    color: white;
}
tbody {
    background-color: #F3F3F3;
    img {
        width: 50%;
    }
}
</style>

