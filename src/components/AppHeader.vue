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
                    link: '#ranking',
                },
                {
                    title: 'LEAGUE TABLE',
                    link: '#ranking', 
                },
                {
                    title: 'PLAYERS',
                    link: '#players', 
                },
                {
                    title: 'GALLERY',
                    link: '#gallery', 
                },
                {
                    title: 'BLOG',
                    link: '#blog', 
                },
                {
                    title: 'CONTACT',
                    link: '#contacts', 
                },
            ],
            arrSlider: [
                {
                    slide: 'src/assets/img/slider1-1.jpg',
                    title: 'Best Game In The World',
                    info: ''
                },
                {
                    slide: 'src/assets/img/slider2-1.jpg',
                    title: 'Sport Club',
                    info: ''
                },
                {
                    slide: 'src/assets/img/slider3.jpg',
                    title: 'Football Club',
                    info: 'Private football matches'
                },
                {
                    slide: 'src/assets/img/slider4.jpg',
                    title: 'I Just Can Get Enough',
                    info: 'Join the club'
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
                    <app-nav v-for="title in arrList" :key="title.title" :title="title.title" :link="title.link" />
                </ul>
            </nav>
        </div>
        <div id="carouselExample" class="carousel slide">
            <div class="carousel-inner">
                <div class="carousel-item active" v-for="(slide, index) in arrSlider" :key="index">
                    <img :src="slide.slide" class="d-block w-100" alt="...">
                    <div class="carousel-caption d-none d-md-block">
                        <h1>{{ slide.title }}</h1>
                        <p>{{ slide.info }}</p>
                        <button>Learn more &rightarrow;</button>
                    </div>
                </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
            </button>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    width: 100%;
    position: relative;

    .black {
        background-color: rgba($color: #000000, $alpha: 0.5);
        z-index: 9;
        position: absolute;
        top: 0;
        right: 0;
        left: 0;
        .icon {
            font-size: 2rem;
            margin-left: 10px;
            color: white;
        }
    }
    .carousel-item {
        position: relative;
        .carousel-caption {
            position: absolute;
            top: 40%;
            h1 {
                font-weight: 700;
                font-size: 4rem;
                @media (max-width: 768px) {
                    font-size: 2rem;
                }
            }
            button {
                background-color: transparent;
                border-radius: 1.3rem;
                padding: .7rem;
                color: white;
                border: 2px solid white;
                margin-top: 1rem;
                font-weight: 600;
                @media (max-width: 768px) {
                    font-size: 1rem;
                }
            }
        }
    }
    
    
}    
</style>