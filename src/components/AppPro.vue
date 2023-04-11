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
        
    </div>
</template>


<style lang="scss" scoped>
    
.bg-img {
    padding: 100px 0;
    background-image: url(img/avadabarbers-about-introbackground.jpg);
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

    .meet-barber {

        button {
            padding: 10px 23px;
            font-size: 12px;
            font-weight: bold;
            color: #c2965b;
            border: 2px solid #c2965b;
            background-color: transparent;
            cursor: pointer;
        }
    }

}

</style>