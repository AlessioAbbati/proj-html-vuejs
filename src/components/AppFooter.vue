<script>
import AppEducation from './AppEducation.vue'
import AppQuickLinks from './AppQuickLinks.vue'
export default {
  components: { AppEducation, AppQuickLinks },
    data() {
        return {
            arrList1: [
                
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
            ],
            arrList2: [
                {
                    title: 'HOME',
                    link: '#' ,
                },
                {
                    title: 'BLOG',
                    link: '#',
                },
                {
                    title: 'CONTACT',
                    link: '#',
                },
            ],
        }
    }

}
</script>

<template>
  <footer>
    <div class="container-fluid text-center">
        <div class="row">
            <div class="col-md-3">
                <div class="content d-flex flex-column">
                    <div class="img d-flex justify-content-start">
                        <img src="../assets/img/logo-footer-football.png" alt="">
                    </div>
                    <div class="info">
                        <span class="d-flex align-items-center justify-content-start">
                            <i class="fa-solid fa-location-dot"></i>
                            <span>New Jersey, USA</span>
                        </span>
                        <span class="d-flex align-items-center justify-content-start">
                            <font-awesome-icon :icon="['fas', 'phone-volume']" />
                            <span>+1 (234) 567 89 10</span>
                        </span>
                        <span class="d-flex align-items-center justify-content-start">
                            <font-awesome-icon :icon="['far', 'envelope']" />
                            <span>example@example.com</span>
                        </span>
                    </div>
                    <div class="socials d-flex justify-content-around">
                        <div class="icon">
                            <font-awesome-icon :icon="['fab', 'facebook-f']" />
                        </div>
                        <div class="icon">
                            <font-awesome-icon :icon="['fab', 'instagram']" />
                        </div>
                        <div class="icon">
                            <font-awesome-icon :icon="['fab', 'twitter']" />
                        </div>
                    </div>
                </div>
            </div>
            <div class="col-md-5">
                <div class="content d-flex flex-column ">
                    <h1>Join our newsletter</h1>
                    <p>Subscribe to be informed about important developments in our club and football world.</p>
                    <input type="mail" placeholder="Your Email Address">
                    <button>Subscribe &RightArrow;</button>
                </div>
            </div>
            <div class="col-md-2">
                <div class="content">
                    <h2>Education</h2>
                    <ul>
                        <app-education v-for="title in arrList1" :key="title.title" :title="title.title" :link="title.link" />
                    </ul>
                </div>
            </div>
            <div class="col-md-2">
                <div class="content">
                    <h2>Quick Links</h2>
                    <ul>
                        <app-quick-links v-for="title in arrList2" :key="title.title" :title="title.title" :link="title.link" />
                    </ul>
                </div>
            </div>
        </div>
        <small class="text-light">&copy; 2022 Football Club - All Right Reserved.</small>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
    height: 25rem;
    width: 100%;
    background-image: url('../assets/img/footer-bg-football.jpg');
    background-size: cover;

    .content {
        color: white;
        margin: 3rem 1rem;

        .img {
            width: 100%;
            margin-bottom: 1rem;

            img {
                width: 20%;
            }
        }

        .info {
            span {
                margin-bottom: .6rem;
                padding-inline: .6rem;
            }
        }

        .socials {
            font-size: 1.5rem;

            .icon {
                border: 1px solid white;
                padding-inline: 1rem;
            }
        }

        input {
            margin-bottom: .5rem;
            padding: 1rem;
            border-radius: 1rem;
        }

        button {
            padding: 1rem;
            border-radius: 1rem;
        }

        h2 {
            white-space: nowrap;
        }

        ul {
            list-style: square;
        }

    }
}</style>

