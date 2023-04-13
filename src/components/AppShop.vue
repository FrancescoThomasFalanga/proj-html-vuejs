<script>
export default {
    data() {
        return {

            products: [

                {
                    img: "img/brush_dark.png",
                    name: "Brush",
                    price: "$15.00",
                },

                {
                    img: "img/scissors.png",
                    name: "Scissors",
                    price: "$85.00",
                },

                {
                    img: "img/hot_oil_dark.png",
                    name: "Hot Oil",
                    price: "$15.00",
                },

                {
                    img: "img/straight_razor_dark.png",
                    name: "Straight Razor",
                    price: "$30.00",
                },

                {
                    img: "img/hair_tonic.png",
                    name: "Hair Tonic",
                    price: "$15.00",
                },

                {
                    img: "img/hair_gel.png",
                    name: "Hair Gel Argan",
                    price: "$85.00",
                },

                {
                    img: "img/hair_gel_1.png",
                    name: "Hair Gel Keratin",
                    price: "$15.00",
                },

                {
                    img: "img/shaving_gel.png",
                    name: "Shaving Gel",
                    price: "$30.00",
                },

            ],

        }
    },

    methods: {

        // functions for horizzontal scroll 
        scrolll() {
            var left = document.querySelector(".scroll-images");
            left.scrollBy(-500, 0);
        },

        scrollr() {
            var left = document.querySelector(".scroll-images");
            left.scrollBy(500, 0);
        },
        // /functions for horizzontal scroll

    },
}
</script>


<template>

    <div class="flex">

        <!-- TOP SECTION -->
        <div class="top">

            <!-- subtitle -->
            <div class="subtitle">
                <strong>WE HAVE YOU COVERED</strong>
            </div>
            <!-- /subtitle -->


            <!-- title -->
            <div class="text">
                <h2>Avada Grooming Products</h2>
            </div>
            <!-- /title -->

        </div>
        <!-- /TOP SECTION -->


        <!-- MIDDLE SECTION -->
        <div class="middle">

            <div class="main-scroll-div">

                <!-- left arrow -->
                <div>
                    <button class="icon" @click="scrolll('.scroll-images')">
                        <i class="fas fa-angle-double-left"></i>
                    </button>
                </div>
                <!-- /left arrow -->


                <!-- MAIN SLIDER -->
                <div class="cover">
                    <div class="scroll-images">

                        <!-- PRODUCT -->
                        <div class="product child" v-for="product in products">
            
                            <!-- product img -->
                            <div class="product-img">
                                <a href="#">
                                    <img :src="product.img" alt="">
                                </a>
                            </div>
                            <!-- /product img -->
            
                            <!-- product name -->
                            <div class="name">
                                <strong> {{ product.name }} </strong>
                            </div>
                            <!-- /product name -->
            
                            <!-- product price -->
                            <div class="price">
                                <span> {{ product.price }} </span>
                            </div>
                            <!-- /product price -->
            
                        </div>
                        <!-- /PRODUCT -->

                    </div>
                </div>
                <!-- /MAIN SLIDER -->


                <!-- right arrow -->
                <div>
                    <button class="icon" @click="scrollr('.scroll-images')">
                        <i class="fas fa-angle-double-right"></i>
                    </button>
                </div>
                <!-- /right arrow -->

            </div>

        </div>
        <!-- /MIDDLE SECTION -->


        <!-- SHOP BUTTON -->
        <div class="product-shop">
            <button>SHOP OUR PRODUCT RANGE</button>
        </div>
        <!-- /SHOP BUTTON -->


        <!-- Product in ABSOLUTE CENTERED -->
        <div class="centered-product">
    
            <!-- left side -->
            <div class="bg-img">

                <img src="img/avadabarbers-cta-background.jpg" alt="">

                <div class="shaving">
                    <a href="#">
                        <img src="img/shaving_butter.png" alt="">
                    </a> 
                </div>

            </div>
            <!-- /left side -->


            <!-- right side -->
            <div class="infos">
    
                <div class="subtitle">
                    <strong>THIS MONTHS FEATURED PRODUCT</strong>
                </div>

                <div class="text">
                    <h2>Shaving Butter</h2>
                </div>

                <div class="product-info">
                    <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam ullam ut suscipit eius voluptas beatae ex deserunt alias quo repudiandae facilis mollitia unde eos, placeat explicabo dolorem minima. Officia, id.</span>
                </div>
                
                <div class="buy">
                    <button>BUY NOW</button>
                </div>
                
            </div>
            <!-- /right side -->
    
        </div>
        <!-- /Product in ABSOLUTE CENTERED -->

    </div>

</template>


<style lang="scss" scoped>

.main-scroll-div {
    position: relative;
    max-width: 1000px;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;

    // __________________________________________
    .cover {
        position: relative;
        width: 90%;
        height: 60%;

        // __________________________________________
        &::before {
            position: absolute;
            content: "";
            left: 0;
            top: 0;
            z-index: 4;
            height: 100%;
            width: 60px;
            background-image: linear-gradient(90deg, rgba(0, 0, 0, 0.603), transparent);
        }

        // __________________________________________
        &::after {
            position: absolute;
            content: "";
            right: 0;
            top: 0;
            z-index: 4;
            height: 100%;
            width: 60px;
            background-image: linear-gradient(-90deg, rgba(0, 0, 0, 0.603), transparent);
        }

        // __________________________________________
        .scroll-images {
            width: 100%;
            height: auto;
            display: flex;
            justify-content: left;
            overflow: hidden;
            position: relative;
            scroll-behavior: smooth;

            // __________________________________________
            .child {
                min-width: 300px;
                min-height: 450px;
                margin: 1px 10px;
                cursor: pointer;
                overflow: hidden;
            }
        }
    }

    // __________________________________________
    .scroll-images::-webkit-scrollbar {
        -webkit-appearance: none;
    }

    .child-img {
        width: 100%;
        height: 100%;
    }

    // __________________________________________
    .icon {
        color: #c2965b;
        font-size: 50px;
        outline: none;
        border: none;
        padding: 0px 20px;
        cursor: pointer;
    }
}
    
.flex {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-image: url(img/avadabarbers-reviewsbackground.jpg);
    background-repeat: no-repeat;
    background-size: cover;

    .top {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding-top: 5px;

        .subtitle {
            font-size: 12px;
            color: #be9359;
        }

        .text {
            margin-bottom: 15px;
            font-size: 28px;
            color: #b1b1b1;
        }
    }

    .middle {
        display: flex;
        justify-content: center;
        align-items: center;

        .product {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;

            .product-img {
                img {
                    width: 100%;
                    height: 300px;
                    object-fit: cover;

                    &:hover {
                        transition: 400ms linear all;
                        transform: scale(1.1);
                    }
                }
            }

            .name {
                font-size: 22px;
                color: #be9359;
            }

            .price {
                font-size: 14px;
                color: #be9359;
            }
        }
    }

    .product-shop {
            margin: 50px 0 100px;
    }
}

.centered-product {
    position: absolute;
    bottom: 0;
    transform: translateY(90%);
    max-width: 800px;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    border-top: 3px solid #c2965b;
    background-color: #121413;

    .bg-img {
        position: relative;

        img {
            width: 300px;
            height: auto;
        }

        .shaving {
            position: absolute;
            top: 0;

            img:hover {
                transition: 400ms linear all;
                transform: scale(1.2);
            }

        }
    }

    .infos {
        padding: 40px;

        .subtitle {
            font-size: 12px;
            color: #be9359;
        }

        .text {
            margin-bottom: 15px;
            font-size: 28px;
            color: #b1b1b1;
        }

        .product-info {
            font-size: 12px;
            color: #b1b1b1;
        }
    }

}

</style>