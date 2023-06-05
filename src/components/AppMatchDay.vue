<script>
export default {
    props: {
        matchDay: Object,
    }
}
</script>

<template>
    <div class="row">
        <div class="col-sm">
            <div class="content d-flex align-items-center">
                <h2>{{ matchDay.team1 }}</h2>
                <img :src="matchDay.logo1" alt="">
            </div>
        </div>
        <div class="col-sm">
            <div class="content d-flex align-items-center justify-content-center">
                <span class="versus">VS</span>
            </div>
        </div>
        <div class="col-sm">
            <div class="content d-flex align-items-center">
                <img :src="matchDay.logo2" alt="">
                <h2>{{ matchDay.team2 }}</h2>
            </div>
        </div>
        <div class="info d-flex justify-content-center">
            <span>
                <i class="fa-solid fa-calendar-days"></i>
                {{ matchDay.date }}
            </span>
            <span>
                &CirclePlus;
                {{ matchDay.stadium }}
            </span>
        </div>
        <div class="btn">
            <button class="text-light">View Match Details</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.row {
  background-color: white;
  @media (max-width: 768px) {
    flex-direction: column;
  }
  div {
    .content {
      @media (max-width: 768px) {
        justify-content: center;
      }
      h2 {
      white-space: nowrap;
      }
      span {
      font-size: 6rem;
      font-weight: 700;
      @media (max-width: 768px) {
        font-size: 4rem;
      }
      }
    }
  }
  .info {
    font-weight: 700;
    span {
        padding-inline: 2rem;
    }
  }
  .btn {
    margin: 1rem 0 2rem 0;
    button {
        background-color: black;
        padding: .7rem;
        border-radius: 1rem;
    }
  }
}
</style>

