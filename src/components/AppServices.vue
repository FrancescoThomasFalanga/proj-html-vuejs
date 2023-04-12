<script>
export default {
    data() {
        return {

            services: [

                {
                    img: "img/avadabarbers-trimcut-icon-before.png",
                    text: "Trim & Cut",
                    subtitle: "Avada Barbers are experts in the lickety split trim and hair cut. Quick but careful and ridicolously good looking.",
                },
                
                {
                    img: "img/avadabarbers-washndry-icon.png",
                    text: "Wash & Dry",
                    subtitle: "Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxurious fashion.",
                },

                {
                    img: "img/avadabarbers-beardtrim-icon.png",
                    text: "Beard Tidy",
                    subtitle: "Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers.",
                },

            ],

        }
    },
}
</script>


<template>

    <div class="bg-color">

        <div class="centered">
    
            <!-- services text -->
            <div class="services">
    
                <!-- subtitle -->
                <div class="subtitle">
                    <strong>MENS GROOMING</strong>
                </div>
                <!-- /subtitle -->

    
                <!-- title -->
                <div class="text">
                    <h2>Services</h2>
                </div>
                <!-- /title -->

            </div>
            <!-- /services text -->


            <!-- SERVICES INFO -->
            <div class="services-info">

                <!-- various service -->
                <div class="service" v-for="service in services">

                    <!-- service img -->
                    <div class="service-img">
                        <img :src="service.img" alt="">
                    </div>
                    <!-- /service img -->

    
                    <!-- service text -->
                    <div class="text">
                        <h4> {{ service.text }} </h4>
                    </div>
                    <!-- /service text -->

    
                    <!-- service subtitle -->
                    <div class="subtitle">
                        <span> {{ service.subtitle }} </span>
                    </div>
                    <!-- /service subtitle -->

                </div>
                <!-- /various service -->

            </div>
            <!-- /SERVICES INFO -->

            
            <div class="read-about">
                <button>READ ABOUT OUR SERVICES</button>
            </div>
        </div>


        
    </div>

    <div class="bottom">
        <img src="img/triangle.svg" alt="" class="bottom-triangle">
    </div>

</template>


<style lang="scss" scoped>

.bg-color {
    background-color: white;

    .centered {
        max-width: 800px;
        margin: 0 auto;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        gap: 40px;

        .services {

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

        .services-info {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 60px;
            margin-bottom: 60px;


            .service {
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                gap: 20px;

                .service-img {
                    img {
                        width: 80px;
                        height: 80px;
                        object-fit: contain;

                        &:hover {
                            transition: 400ms linear all;
                            transform: scale(1.2);
                            cursor: pointer;
                        }
                    }
                }

                .text {
                    font-size: 22px;
                    color: #be9359;
                }

                .subtitle {
                    font-size: 14px;
                    text-align: center;
                    color: #b1b1b1;
                }

            }

        }

        .read-about {
            margin-bottom: 100px;
        }
    }

}
.bottom {
    background-color: #fff;
    .bottom-triangle {
        filter: invert(0.92);
        width: 100%;
        height: 100px;
        margin-bottom: -6px;
    }

}

</style>