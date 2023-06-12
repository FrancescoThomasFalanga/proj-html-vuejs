<script>
export default {
    data() {
        return {

            isHome: 0,

            navLinks: ["Home", "About Us", "Services", "Shop", "Our Team", "Blog", "Contact Us"],
            
        }
    },

    methods: {

        hamburgerMenu() {

            const hamburger = document.querySelector(".hamburger");
            const navMenu = document.querySelector(".nav-menu");

            hamburger.classList.toggle("active");
            navMenu.classList.toggle("active");

        },

    }
}
</script>


<template>
    <div class="bg-img">

        <!-- RIGHT ABSOLUTE LINKS -->
        <div class="absolute">

            <!-- demos -->
            <div class="demos">
                <div class="price">
                    <i class="fa-solid fa-wallet"></i>
                </div>
                <div class="text">
                    <span>Demos</span>
                </div>
            </div>
            <!-- /demos -->


            <!-- on-sale -->
            <div class="on-sale">
                <div class="price">
                    <strong class="dollar">$</strong>
                    <strong>39</strong>
                </div>
                <div class="text">
                    <span>On Sale</span>
                </div>
            </div>
            <!-- /on-sale -->

        </div>
        <!-- /RIGHT ABSOLUTE LINKS -->
        

        <!-- TOP section -->
        <div class="fixed">

            <div class="flex">
    
                <!-- logo section -->
                <div class="logo">
                    <a href="#"><img src="../../img/avadabarbers-logo-x1.png" alt=""></a>
                </div>
                <!-- /logo section -->
    
    
                <!-- navbar section -->
                <div class="links">
    
                    <!-- cart menu -->
                    <div class="cart">
                        <i class="fa-solid fa-cart-shopping"></i>
                    </div>
                    <!-- /cart menu -->
    
    
                    <!-- HAMBURGER MENU SECTION -->
                    <div class="hamburger-menu" @click="hamburgerMenu()">
    
                        <!-- menu & menu items -->
                        <ul class="nav-menu">
                            <li class="nav-item" v-for="(link, index) in navLinks">
                                <a href="#" class="nav-link" @click="isHome = index" :class="index == isHome ? 'home' : '' "> {{ link }} </a>
                            </li>
                        </ul>
                        <!-- /menu & menu items -->
                        
    
                        <!-- menu bars -->
                        <div class="hamburger">
                            <span class="bar"></span>
                            <span class="bar"></span>
                            <span class="bar"></span>
                        </div>
                        <!-- /menu bars -->
    
                    </div>
                    <!-- HAMBURGER MENU SECTION -->
    
                </div>
                <!-- /navbar section -->
    
            </div>

        </div>
        <!-- /TOP section -->


        <!-- MIDDLE section -->
        <div class="flex padding">

            <!-- middle left header -->
            <div class="text">

                <!-- title -->
                <div class="title">
                    <h1>Barber Shop</h1>
                </div>

                <!-- horizzontal line -->
                <div class="horizzontal-line"></div>

                <!-- subtitle -->
                <div class="subtitle">
                    <span>The Pinnacle of Male Grooming</span>
                </div>

                <!-- BUTTON LEARN MORE -->
                <div class="learn-more">
                    <button>LEARN MORE</button>
                </div>

            </div>
            <!-- /middle left header -->


            <!-- middle right header -->
            <div class="img-header">

                <img src="../../img/avadabarbers_hero_focalmirror.png" alt="img-header">

            </div>
            <!-- /middle right header -->

        </div>
        <!-- /MIDDLE section -->
        
    </div>
</template>


<style lang="scss" scoped>

.bg-img {
    position: relative;
    padding: 20px 0 100px;
    background-image: url(../../img/avadabarbers-homepage-hero-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;

    .absolute {
        position: fixed;
        right: 15px;
        top: 100px;
        z-index: 3;

        .demos, .on-sale {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 5px 10px;
            margin-bottom: 5px;
            border-radius: 10px;
            color: #656c72;
            background-color: #ffffff;
            cursor: pointer;

            .price {
                font-size: 24px;
                color: #33475b;
            }
            
            .text {
                font-size: 12px;
                font-weight: bold;
            }
        }

        .on-sale {
            .price {
                position: relative;
                color: #65bc7b;

                .dollar {
                    position: absolute;
                    top: 0;
                    left: -8px;
                    font-size: 14px;
                }

            }
        }

    }
    
}
    
.fixed {
    position: fixed;
    padding: 10px 0;
    top: 0;
    left: 0;
    right: 0;
    z-index: 4;
    background-color: rgba(0, 0, 0, 0.8);
}

.padding {
    padding-top: 80px;
}


 .flex {
    max-width: 800px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;


    .logo {
        img {
            width: 120px;
        }
    }


    .links {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 15px;

        .cart {
            font-size: 11px;
            cursor: pointer;
        }

        .hamburger-menu {

            li {
                list-style-type: none;
            }
    
            a {
                text-decoration: none;
            }
    
            .hamburger {
                display: none;

                .bar {
                    display: block;
                    width: 25px;
                    height: 3px;
                    margin: 5px auto;
                    -webkit-transition: all 0.3s ease-in-out;
                    transition: all 0.3s ease-in-out;
                    background-color: #fff;
                }
            }
    
            .nav-menu {
                display: flex;
                justify-content: center;
                align-items: center;
                position: fixed;
                z-index: 2;
                left: -100%;
                top: 0;
                flex-direction: column;
                background-color: #020202bd;
                width: 100%;
                height: 100%;
                border-radius: 10px;
                text-align: center;
                transition: 0.3s;
                box-shadow:
                    0 10px 27px rgba(0, 0, 0, 0.05);
        
                .nav-link{
                    font-size: 1.2rem;
                    font-weight: bold;
                    color: #fff;
                }
        
                .nav-link:hover{
                    transition: 500ms linear all;
                    color: #c2965b;
                }
        
                .home {
                    color: #c2965b;
                }
            }
    
    
            .nav-menu.active {
                    left: 0;
            }
    
            .nav-item {
                margin: 1.1rem 0;
            }
    
            .hamburger {
                display: block;
                cursor: pointer;
            }
    
            .hamburger.active .bar:nth-child(2) {
                opacity: 0;
            }
    
            .hamburger.active .bar:nth-child(1) {
                transform: translateY(8px) rotate(45deg);
            }
    
            .hamburger.active .bar:nth-child(3) {
                transform: translateY(-8px) rotate(-45deg);
            }


        }

    }


    .text {

        .title {
            font-size: 26px;
        }
        
        .horizzontal-line {
            margin: 20px 0;
            width: 50%;
            height: 2px;
            background-color: #c2965b;
        }

        .subtitle {
            margin-bottom: 20px;
            color: #383634;
        }
    }


    .img-header {
        img {
            width: 100%;
            height: 500px;
        }
    }
 }

</style>