<script>
export default {
  props: {
    match: Object,
  }
}
</script>

<template>
  <div class="row">
    <div class="col-sm d-flex align-items-center">
      <h2>Instanbul Sports</h2>
      <img :src="match.logo1" alt="">
    </div>
    <div class="col-sm d-flex align-items-center justify-content-center">
      <span>VS</span>
    </div>
    <div class="col-sm d-flex align-items-center">
      <img :src="match.logo2" alt="">
      <h2>United Fs Club</h2>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.row {
  div {
    h2 {
    white-space: nowrap;
    }
    span {
    font-size: 6rem;
    font-weight: 700;
    }
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