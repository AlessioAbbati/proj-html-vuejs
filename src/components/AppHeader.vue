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
        <div class="black">
            <div class="logos d-flex align-items-center justify-content-center">
                <div class="img">
                        <img src="../assets/img/sponsor1.png" alt="">
                </div>
                <div class="img">
                        <img src="../assets/img/sponsor2.png" alt="">
                </div>
                <div class="img">
                        <img src="../assets/img/logo-football.png" alt="">
                </div>
                <font-awesome-icon class="icon" :icon="['fab', 'facebook-f']" />
                <font-awesome-icon class="icon" :icon="['fab', 'instagram']" />
                <font-awesome-icon class="icon" :icon="['fab', 'twitter']" />
            </div>
            <nav>
                <ul class="list-unstyled d-flex justify-content-center">
                    <app-nav 
                        v-for="title in arrList" 
                        :key="title.title" 
                        :title="title.title" 
                        :link="title.link"  
                    />
                </ul>
            </nav>
        </div>
        <div class="carousel d-flex justify-content-between align-items-center">
            <div class="chevron_circle">
                <font-awesome-icon class="chevron" :icon="['fas', 'chevron-left']" />
            </div>
            <div class="text d-flex flex-column align-items-center">
                <h1>Football Club</h1>
                <h1>Sport club</h1>
                <small>Private football matches</small>
                <button><small>Learn More</small></button>
            </div>
            <div class="chevron_circle">
                <font-awesome-icon class="chevron" :icon="['fas', 'chevron-right']" />
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    height: 40rem;
    width: 100%;
    background-image: url('../assets/img/slider2-1.jpg');
    background-size: cover;

    .black {
        background-color: rgba($color: #000000, $alpha: 0.5);
        .icon {
            font-size: 2rem;
            margin-left: 10px;
            color: white;
        }
    }
    .carousel {
        margin-top: 3rem;
        .text {
        color: white;
        h1 {
            font-size: 4rem;
            font-weight: 700;
        }
        button {
            background-color: transparent;
            border-radius: 1.3rem;
            padding: .7rem;
            color: white;
            border: 2px solid white;
            margin-top: 1rem;
            font-weight: 600;
        }
    }
        .chevron_circle {
            position: relative;
            width: 70px;
            height: 70px;
           .chevron {
                color: white;
                border: 1px solid white;
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                border-radius: 50%;
                width: 50px;
                height: 50px;
                box-sizing: border-box;
           }
        }
    }
}
</style>

