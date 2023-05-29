<script>
import AppNav from './AppNav.vue'
export default {
  components: { AppNav },
  data() {
        return {
            arrList: [
                {
                    title: 'HOME',
                    link: '#' ,
                },
                {
                    title: 'FIXTURES & RESULTS',
                    link: '#',
                },
                {
                    title: 'LEAGUE TABLE',
                    link: '#', 
                },
                {
                    title: 'PLAYERS',
                    link: '#', 
                },
                {
                    title: 'GALLERY',
                    link: '#', 
                },
                {
                    title: 'BLOG',
                    link: '#', 
                },
                {
                    title: 'CONTACT',
                    link: '#', 
                },
            ]
            
        }
    }

};
</script>

<template>
  <header>
    <div class="logos">
    <img src="../assets/img/sponsor1.png" alt="">
    <img src="../assets/img/sponsor2.png" alt="">
    <img src="../assets/img/logo-football.png" alt="">
    <!-- <font-awesome-icon class="icon" :icon="['fab', 'facebook-f']" />
    <font-awesome-icon class="icon" :icon="['fab', 'instagram']" />
    <font-awesome-icon class="icon" :icon="['fab', 'twitter']" /> -->
    <app-nav 
        v-for="title in arrList" 
        :key="title.title" 
        :title="title.title" 
        :link="title.link" 
    />
  </div>
  </header>
</template>

<style lang="scss" scoped>
header {
    height: 45rem;
    width: 100%;
    background-image: url('../assets/img/slider2-1.jpg');
    background-size: contain;
    background-size: cover;
    .logos {
        background-color: rgba($color: #000000, $alpha: 0.5);
    }
}
</style>

