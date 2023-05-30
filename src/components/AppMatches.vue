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
      <div class="content d-flex align-items-center">
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
    <div class="info d-flex justify-content-center text-light">
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
  div {
    .content {
      
      h2 {
      white-space: nowrap;
      color: white;
      }
      span {
      font-size: 3rem;
      color: white;
      font-weight: 700;
      }
    }
  }
  .info {
    background-color: rgba($color: #000000, $alpha: 0.5);
  }
}
</style>

<!-- <div class="container">
      <div class="row">
        <div class="col-sm d-flex align-items-center">
          <h2>Instanbul Sports</h2>
          <img src="../assets/img/club-1.png" alt="">
        </div>
        <div class="col-sm d-flex align-items-center justify-content-center">
          <p>VS</p>
        </div>
        <div class="col-sm d-flex align-items-center">
          <img src="../assets/img/club-2.png" alt="">
          <h2>United Fs Club</h2>
        </div>
      </div>
    </div> -->