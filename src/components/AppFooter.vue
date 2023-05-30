<script></script>

<template>
  <footer>
    <div class="container-fluid">
        <div class="row">
            <div class="col-md-3">
                <div class="content d-flex flex-column">
                    <div class="img">
                        <img src="../assets/img/logo-footer-football.png" alt="">
                    </div>
                    <div class="info">
                        <span class="d-flex align-items-center justify-content-start">
                            <font-awesome-icon :icon="['fas', 'location-dot']" />
                            <font-awesome-icon :icon="['fas', 'location-pin']" />
                            <p>New Jersey, USA</p>
                        </span>
                        <span class="d-flex align-items-center justify-content-start">
                            <font-awesome-icon :icon="['fas', 'phone-volume']" />
                            <p>+1 (234) 567 89 10</p> 
                        </span>
                        <span class="d-flex align-items-center justify-content-start">
                            <font-awesome-icon :icon="['far', 'envelope']" />
                            <p>example@example.com</p>
                        </span>
                    </div>
                    <div class="socials d-flex justify-content-around">
                        <font-awesome-icon class="icon" :icon="['fab', 'facebook-f']" />
                        <font-awesome-icon class="icon" :icon="['fab', 'instagram']" />
                        <font-awesome-icon class="icon" :icon="['fab', 'twitter']" />
                    </div>
                </div>              
            </div>
            <div class="col-md-5">
                <div class="content">
                    
                </div>
            </div>
            <div class="col-md-2">
                <div class="content">
                    
                </div>
            </div>
            <div class="col-md-2">
                <div class="content">
                    
                </div>
            </div>
        </div>
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
        border: 1px solid white;
        .info {
            span {
                vertical-align: middle;
            }
        }
        .socials {
            font-size: 1.5rem;
            .icon {
                border: 1px solid white;
                
            }
        }
    }
}
</style>

