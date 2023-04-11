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

            ],

        }
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

            <!-- PRODUCT -->
            <div class="product" v-for="product in products">

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
        <!-- /MIDDLE SECTION -->


        <!-- SHOP BUTTON -->
        <div class="product-shop">
            <button>SHOP OUR PRODUCT RANGE</button>
        </div>
        <!-- /SHOP BUTTON -->

    </div>

</template>


<style lang="scss" scoped>
    
.flex {
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
                        transform: scale(1.2);
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
        button {
            padding: 10px 23px;
            font-size: 12px;
            font-weight: bold;
            color: #c2965b;
            border: 2px solid #c2965b;
            background-color: transparent;
            cursor: pointer;
            margin: 50px 0 100px;
        }
    }
}

</style>