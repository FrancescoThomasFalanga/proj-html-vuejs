<script>
export default {
    data() {
        return {

            credits: ["Avada Barbers", "123 New York Street", "New York City", "info@yourwebsite.com", "+1 (555) 555-1212"],

        }
    },

    methods: {

        goUp() {

            scrollTo({
                top: 0,
                behavior: "smooth",
            })
        },
    },
}
</script>


<template>

    <div class="fixed">

        <div class="bg-color-primary">
            
            <!-- /centered container  -->
            <div class="centered-container">
    
                <!-- LEFT SECTION -->
                <div class="left-side">
                    
                    <!-- left side img -->
                    <div class="left-img">
                        <a href="#">
                            <img src="img/avadabarbers_footer_shop_image.png" alt="">
                        </a>
                    </div>
                    <!-- /left side img -->
    
    
                    <!-- BUTTON  -->
                    <div class="shop-button">
                        <button>SHOP OUR RANGE NOW</button>
                    </div>
                    <!-- /BUTTON  -->
    
                </div>
                <!-- /LEFT SECTION -->
    
    
                <!-- MIDDLE SECTION -->
                <div class="middle-side">
    
                    <!-- middle side img -->
                    <div class="middle-img">
                        <a href="#">
                            <img src="img/avadabarbers-logo-x1.png" alt="">
                        </a> 
                    </div>
                    <!-- /middle side img -->
    
    
                    <!-- infos about the place  -->
                    <div class="credits">
                        <ul>
                            <li v-for="credit in credits"> {{ credit }} </li>
                        </ul>
                    </div>
                    <!-- /infos about the place  -->
    
    
                    <!-- follow wheeeere -->
                    <div class="follow">
                        <strong>FOLLOW US</strong>
                    </div>
                    <!-- /follow wheeeere -->
    
    
                    <!-- social  -->
                    <div class="social">
                        <a href="#">
                            <i class="fa-brands fa-facebook-f"></i>
                        </a> 
                        <a href="#">
                            <i class="fa-brands fa-twitter"></i>
                        </a> 
                        <a href="#">
                            <i class="fa-brands fa-youtube"></i>
                        </a> 
                        <a href="#">
                            <i class="fa-brands fa-instagram"></i>
                        </a> 
                    </div>
                    <!-- /social  -->
    
                </div>
                <!-- /MIDDLE SECTION -->
    
    
                <!-- RIGHT SECTION -->
                <div class="right-side">
    
                    <!-- right side img  -->
                    <div class="right-img">
                        <a href="#">
                            <img src="img/avadabarbers_footer_appointment_image.png" alt="">
                        </a>
                    </div>
                    <!-- /right side img  -->
    
    
                    <!-- BUTTON -->
                    <div class="appointment-button">
                        <button>BOOK YOUR APPOINTMENT</button>
                    </div>
                    <!-- /BUTTON -->
    
                </div>
                <!-- /RIGHT SECTION -->
    
            </div>
            <!-- /centered container  -->
    
        </div>
        <!-- /UPPER FOOTER -->
    
    
    
        <!-- BOTTOM FOOTER -->
        <div class="bg-color-secondary">
    
            <div class="copyright">
                <span>@ Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by CICCIO</span>
            </div>
    
        </div>
        <!-- /BOTTOM FOOTER -->


        <div class="absolute" @click="goUp()">
            <button class="go-up">
                <i class="fa-solid fa-chevron-up"></i>
            </button>
        </div>

    </div>


</template>


<style lang="scss" scoped>

.fixed {
    position: relative;
}

.absolute {
    position: absolute;
    bottom: 0;
    right: 10%;

    button {
        border: none;
        padding: 14px;
        color: white;
        font-size: 18px;
        background-color: #303030;

        &:hover {
            background-color: #ad8652;
        }
    }
}

.bg-color-primary {
    background-color: #121314;
    padding: 20px 0;

    .centered-container {
        max-width: 800px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .left-side, .right-side {
            margin-top: 60px;
            
            .left-img, .right-img {
                img {
                    width: 200px;
                    height: auto;
                    object-fit: contain;
                }
            }

            button {
                margin-bottom: 50px;
            }

        }

        .middle-side {
            text-align: center;

            .middle-img {
                img {
                    margin-bottom: 40px;
                    width: 150px;
                }
            }

            .credits {
                ul {
                    list-style-type: none;
                    text-align: center;

                    li {
                        font-size: 14px;
                        color: #b1b1b1be;
                    }
                }
            }

            .follow {
                padding: 30px 0 10px;
                color: #be9359;
            }

            .social {
                display: flex;
                justify-content: center;
                align-items: center;
                gap: 12px;

                i {
                    color: #bebdbd;
                }
            }

        }
    }
}


.bg-color-secondary {
    background-color: #161718;
    padding: 40px 0;

    .copyright {
        text-align: center;
        font-size: 14px;
        color: #474a4d;
    }
}


</style>