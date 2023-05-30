<script>
export default {
    props: {
        info: Object,
    }
}
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-sm d-flex align-items-center">
                <img :src="info.logo1" alt="">
                <h2>{{ info.team1 }}</h2>
            </div>
            <div class="col-sm d-flex align-items-center justify-content-center">
                <p>VS</p>
            </div>
            <div class="col-sm d-flex align-items-center">
               <h2>{{ info.team2 }}</h2>
               <img :src="info.logo2" alt="">
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>


