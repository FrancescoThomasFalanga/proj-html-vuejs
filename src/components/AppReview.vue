<script>
export default {
    data() {
        return {

            reviews: [

                {
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt architecto eligendi facere dolorem rerum ratione libero fugit et quisquam! Beatae saepe minima soluta. Et, quia dolorem corporis facilis adipisci repudiandae?",
                    img: "img/avadabarbers-trimcut-gallery6.jpg",
                    name: "John Doe",
                },

                {
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt architecto eligendi facere dolorem rerum ratione libero fugit et quisquam! Beatae saepe minima soluta. Et, quia dolorem corporis facilis adipisci repudiandae?",
                    img: "img/avadabarbers-trimcut-gallery7.jpg",
                    name: "Pete Jones",
                },

                {
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt architecto eligendi facere dolorem rerum ratione libero fugit et quisquam! Beatae saepe minima soluta. Et, quia dolorem corporis facilis adipisci repudiandae?",
                    img: "img/avadabarbers-trimcut-gallery3.jpg",
                    name: "Mark Wilson",
                },

            ],

        }
    }
}
</script>


<template>

    <div class="bg-color">

        <!-- MAX WIDTH CONTAINER -->
        <div class="centered-container">

            <!-- SUBTITLE AND TITLE -->
            <div class="reviews-info">

                <!-- subtitle -->
                <div class="subtitle">
                    <strong>WHAT PEOPLE SAY</strong>
                </div>
                <!-- /subtitle -->


                <!-- title -->
                <div class="text">
                    <h2>Reviews</h2>
                </div>
                <!-- /title -->

            </div>
            <!-- /SUBTITLE AND TITLE -->


            <!-- CARDS CONTAINER -->
            <div class="reviews">
                
                <!-- CARD -->
                <div class="review" v-for="review in reviews">

                    <!-- profile info -->
                    <div class="info">
                        <span> {{ review.text }} </span>
                    </div>
                    <!-- /profile info -->


                    <!-- profile img -->
                    <div class="border-img">
                        <a href="#">
                            <img :src="review.img" alt="">
                        </a>
                    </div>
                    <!-- /profile img -->


                    <!-- profile name -->
                    <div class="name">
                        <h4> {{ review.name }} </h4>
                    </div>
                    <!-- /profile name -->

                </div>
                <!-- /CARD -->

            </div>
            <!-- /CARDS CONTAINER -->

        </div>
        <!-- /MAX WIDTH CONTAINER -->

    </div>


</template>


<style lang="scss" scoped>
    
.bg-color {
    background-color: #fff;
}

.centered-container {
    max-width: 800px;
    margin: 0 auto;
    padding-top: 400px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;

    .reviews-info {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

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

    .reviews {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 50px;
        padding-bottom: 50px;

        .review {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            gap: 8px;

            .info {
                text-align: center;
                font-size: 12px;
                color: #b1b1b1;
            }

            .border-img {
                img {
                    width: 80px;
                    border-radius: 50%;

                    &:hover {
                        transition: 1s linear all;
                        transform: scale(1.1);
                    }
                }
            }

            .name {
                font-style: italic;
                color: #be9359;
            }
        }
    }
}

</style>