<template>
    <div class="offers">
        <div class="container">
            <h2 class="title">мы всегда в топе!</h2>
            <p class="info">Мы прямой рекламодатель с собственными офферами, которые входят в топ-чарты AppStore и Google Play. </p>
            <div class="row">
                <div class="offer">
                    <span class="offer__name">топ</span>
                    <span class="offer__info">Наши офферы входят в ТОПы в AppStore и Google Play</span>
                </div>
                <div class="offer">
                    <span class="offer__name">оффер</span>
                    <span class="offer__info">Наши офферы входят в ТОПы в AppStore и Google Play</span>
                </div>
                <div class="offer">
                    <span class="offer__name">2.5 <span>$</span></span>
                    <span class="offer__info">Наши офферы входят в ТОПы в AppStore и Google Play</span>
                </div>
            </div>
        </div>
        <Particles
                id="tsparticles"
                :particlesInit="particlesInit"
                :particlesLoaded="particlesLoaded"
                :options="option"
        />
    </div>
</template>

<script>

export default {
    name : "Offer",
    props : {
        option : {
            type : Object,
            default : () => {}
        }
    }
}
</script>

.<style lang="scss">
.offers{
    position: relative;
    background-image: url('../assets/images/bg2.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    padding: 136px 0;
    .title{
        color: white;
    }
    .info{
        color: white;
        margin: 20px 0 80px;
        font-weight: 400;
    }
    .row{
        justify-content: center;
        flex-wrap: wrap;
        gap: 34px;
    }
    .offer{
        display: flex;
        align-items: center;
        flex-direction: column;
        gap: 36px;
        &__name{
            font-weight: 900;
            font-size: 72px;
            line-height: 80px;
            text-transform: uppercase;
            color: #FFFFFF;
            span{
                font-size: 42px;
                margin-left: -12px;
            }
        }
        &__info{
            font-weight: bold;
            font-size: 16px;
            line-height: 19px;
            text-align: center;
            color: #FFFFFF;
            font-weight: 400;
        }
    }
}

@media(max-width:500px){
    .offers{
        background-size: 600%;
        .row{
            flex-direction: column;
        }
    }
}
</style>