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
                <div class="info">{{ info.team1 }}</div>
            </div>
        </div>
        <div class="col-sm">
            <div class="content d-flex justify-content-center align-items-center">
                <span>VS</span>
            </div>
        </div>
        <div class="col-sm">
            <div class="content d-flex align-items-center">
                <div class="info">{{ info.team2 }}</div>
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

            .info {
                white-space: nowrap;
            }

        }

    }
}
</style>


