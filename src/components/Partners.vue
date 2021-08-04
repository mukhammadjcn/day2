<template>
    <div class="partners">
        <div class="container">
            <h2 class="title">Нам доверяют</h2>
            <div class="row">
                <img src="../assets/images/p1.png" alt="">
                <img src="../assets/images/p2.png" alt="">
                <img src="../assets/images/p3.png" alt="">
                <img src="../assets/images/p4.png" alt="">
                <img src="../assets/images/p5.png" alt="">
                <img src="../assets/images/p6.png" alt="">
                <img src="../assets/images/p7.png" alt="">
                <img src="../assets/images/p8.png" alt="">
                <img src="../assets/images/p9.png" alt="">
                <img src="../assets/images/p10.png" alt="">
                <img src="../assets/images/p11.png" alt="">
                <img src="../assets/images/p12.png" alt="">
                <img src="../assets/images/p13.png" alt="">
                <img src="../assets/images/p14.png" alt="">
                <img src="../assets/images/p15.png" alt="">
                <img src="../assets/images/p16.png" alt="">
            </div>
            <p class="info">и десятки других популярных компаний</p>
        </div>
    </div>
</template>

<script>
export default {
    name : "Partners"
}
</script>

<style lang="scss">
.partners{
    .row{
        margin: 84px 0;
        flex-wrap: wrap;
        row-gap: 60px;
        column-gap: 50px;
        justify-content: center;
    }
    .info{
        color: #939393;
    }
}

@media (max-width:500px) {
    .partners{
        .row{
            column-gap: 16px;
            row-gap: 28px;
            img{
                width: 36%;
                flex-basis: 20%;
            }
        }
    }
}
</style>