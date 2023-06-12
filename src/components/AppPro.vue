<script>
export default {
    data() {
        return {

        }
    },
}
</script>


<template>
    <div class="bg-img">

        <div>
            <div class="subtitle">
                <strong>AWARD WINNING</strong>
            </div>

            <div class="text">
                <h2>Pro Barbers</h2>
            </div>

            <div class="meet-barber">
                <button>MEET YOUR NEW BARBER</button>
            </div>
        </div>

        <img src="/img/triangle.svg" alt="">

    </div>
</template>


<style lang="scss" scoped>
.bg-img {
    position: relative;
    padding: 100px 0 200px;
    background-image: url(/img/avadabarbers-about-introbackground.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    text-align: center;

    .subtitle {
        font-size: 12px;
        color: #be9359;
    }

    .text {
        margin-bottom: 15px;
        font-size: 28px;
        color: #b1b1b1;
    }

    img {
        position: absolute;
        bottom: -50px;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 100%;
        height: 100px;
    }

}
</style>