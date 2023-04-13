<script>
export default {
    data() {
        return {

            blogs: [

                {
                    img: "img/avadabarbers-second-blog-320x202.jpg",
                    name: "Avada Barbers Now Open",
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt architecto eligendi facere dolorem rerum ratione libero fugit et quisquam! Beatae saepe minima soluta. Et, quia dolorem corporis facilis adipisci repudiandae?",
                },

                {
                    img: "img/avadabarbers-choosing-blog-320x202.jpg",
                    name: "Choosing The Right Barber",
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt architecto eligendi facere dolorem rerum ratione libero fugit et quisquam! Beatae saepe minima soluta. Et, quia dolorem corporis facilis adipisci repudiandae?",
                },

                {
                    img: "img/avadabarbers-ourservice-blog-320x202.jpg",
                    name: "Quick Service Guide",
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt architecto eligendi facere dolorem rerum ratione libero fugit et quisquam! Beatae saepe minima soluta. Et, quia dolorem corporis facilis adipisci repudiandae?",
                },

            ],

        }
    }
}
</script>


<template>

    <div class="bg-color">

        <!-- WAVE -->
        <div>
            <img src="img/triangle.svg" alt="" class="bottom-triangle">
        </div>
        <!-- /WAVE -->

        
        <!-- CENTERED CONTAINER -->
        <div class="centered-container">

            <!-- blogs text -->
            <div class="blogs-text">

                <!-- blogs subtitle  -->
                <div class="subtitle">
                    <strong>TALES FROM THE BARBER SHOP</strong>
                </div>

                <!-- blogs title  -->
                <div class="text">
                    <h2>Recent Blog Posts</h2>
                </div>

            </div>
            <!-- /blogs text -->


            <!-- BLOGS CARD -->
            <div class="blogs">

                <!-- CARD -->
                <div class="blog" v-for="blog in blogs">

                    <!-- card img -->
                    <div class="blog-img">
                        <a href="#">
                            <img :src="blog.img" alt="">
                        </a>
                    </div>
                    <!-- /card img -->


                    <!-- card name -->
                    <div class="name">
                        <a href="#">
                            <h4> {{ blog.name }} </h4>
                        </a> 
                    </div>
                    <!-- /card name -->


                    <!-- card text -->
                    <div class="text">
                        <span> {{ blog.text }} </span>
                    </div>
                    <!-- /card text -->

                </div>
                <!-- /CARD -->

            </div>
            <!-- /BLOGS CARD -->


            <!-- BUTTON -->
            <div class="read-more">
                <button>READ MORE FROM OUR BLOG</button>
            </div>
            <!-- /BUTTON -->

        </div>
        <!-- /CENTERED CONTAINER -->

    </div>

</template>


<style lang="scss" scoped>


.bg-color {
    background-color: #f5f5f5;

    .bottom-triangle {
        transform: rotate(180deg);
        width: 100%;
        height: 100px;
    }
    
    .centered-container {
        padding-top: 60px;
        max-width: 800px;
        margin: 0 auto;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        gap: 40px;

        .blogs-text {
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

        .blogs {
            display: flex;
            justify-content: center;
            align-items: flex-start;
            gap: 20px;

            .blog {
                display: flex;
                justify-content: center;
                align-items: center;
                flex-direction: column;
                text-align: center;

                .blog-img {
                    img {
                        width: 100%;
                        border-radius: 10px;
                    }
                }

                .name {
                    margin: 2px 0 5px;
                    font-size: 23px;

                    a {
                        text-decoration: none;
                        color: #be9359;

                        &:hover {
                            text-decoration: underline;
                        }
                    }

                }

                .text {
                    text-align: center;
                    font-size: 14px;
                    color: #b1b1b1;
                }
            }
        }

        .read-more {
            margin-bottom: 100px;
        }
    }
}

</style>