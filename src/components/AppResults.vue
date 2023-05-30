<script>
export default {
    props: {
        info: Object,
    }
}
</script>

<template>
    <div class="row">
        <div class="col-sm">
            <div class="content d-flex align-items-center">
                <img :src="info.logo1" alt="">
                <p>{{ info.team1 }}</p>
            </div>
        </div>
        <div class="col-sm">
            <div class="content d-flex justify-content-center align-items-center">
                <p>VS</p>
            </div>
        </div>
        <div class="col-sm">
            <div class="content d-flex align-items-center">
                <p>{{ info.team2 }}</p>
                <img :src="info.logo2" alt="">
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.row {
    padding-bottom: 1rem;

    div {
        .content {
            img {
                width: 30%;
            }

            p {
                white-space: nowrap;
            }

        }

    }
}
</style>


