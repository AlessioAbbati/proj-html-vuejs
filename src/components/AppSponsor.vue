<script>
export default {
    data() {
        return {
            sponsors: [
                {
                    logo: 'src/assets/img/client2.png',
                },
                {
                    logo: 'src/assets/img/client3.png',
                },
                {
                    logo: 'src/assets/img/client4.png',
                },
                {
                    logo: 'src/assets/img/client7.png',
                },
                {
                    logo: 'src/assets/img/client9.png',
                },
                {
                    logo: 'src/assets/img/client10.png',
                },
            ],
        }
    }
}
</script>

<template>
  <img v-for="sponsor in sponsors" :key="sponsor" :src="sponsor.logo" alt="">
</template>

<style lang="scss" scoped>
 img {
    border: 2px solid white;
    border-radius: 2rem;
    margin-inline: .5rem;
    width: calc((100% / 6) - 2.5rem);
    @media (max-width: 768px) {
        width: calc((100% / 6) - 1rem);
    }
    } 
</style>

