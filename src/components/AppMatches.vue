<script>
export default {
  props: {
    match: Object,
  }
}
</script>

<template>
  <div class="row">
    <div class="col-sm">
      <div class="content d-flex align-items-center justify-content-center">
        <img :src="match.logo1" alt="">
        <h2>{{ match.team1 }}</h2>
      </div>
    </div>
    <div class="col-sm">
      <div class="content d-flex align-items-center justify-content-center">
        <span>VS</span>
      </div>
    </div>
    <div class="col-sm">
      <div class="content d-flex align-items-center">
        <h2>{{ match.team2 }}</h2>
        <img :src="match.logo2" alt="">
      </div>
    </div>
    <div class="info d-flex justify-content-center text-light justify-content-center">
      <span>
        <i class="fa-solid fa-calendar-days"></i>
        {{ match.date }}
      </span>
      <span>
        &CirclePlus;
        {{ match.stadium }}
      </span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.row {
  background-color: rgba($color: #000000, $alpha: 0.2);
  margin-bottom: 1rem;
  div {
    .content {
      img {
        @media (max-width: 768px) {
          width: 30%;
        }
      }
      h2 {
      white-space: nowrap;
      color: white;
      @media (max-width: 768px) {
          font-size: 1.5rem;
        }
      }
      span {
      margin-top: 1rem;
      font-size: 4rem;
      color: white;
      font-weight: 700;
      @media (max-width: 768px) {
        font-size: 1rem;
        margin-top: 1.5rem;
      }
      }
    }
  }
  .info {
    background-color: rgba($color: #000000, $alpha: 0.5);
    span {
      padding-inline: 2rem;
    }
  }
}
</style>