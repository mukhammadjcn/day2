<template>
    <div class="payments">
        <div class="container">
            <div class="title">Еженедельные выплаты <span>от $100</span></div>
            <p class="info">На удобную для вас платежную систему из перечисленных ниже</p>
            <div class="row">
                <a href="/"><img src="../assets/images/z1.png" alt=""></a>
                <a href="/"><img src="../assets/images/z3.png" alt=""></a>
                <a href="/"><img src="../assets/images/z2.png" alt=""></a>
                <a href="/"><img src="../assets/images/z4.png" alt=""></a>
                <a href="/"><img src="../assets/images/z5.png" alt=""></a>
                <a href="/"><img src="../assets/images/z6.png" alt=""></a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name : "Payments",

}
</script>

<style lang="scss">
.payments{
    margin-top: 86px;
    .info{
        margin-top: 20px;
        color: #939393;
    }
    .row{
        margin: 84px 0;
        flex-wrap: wrap;
        gap: 30px;
        justify-content: space-between;
    }
}

@media (max-width:500px) {
    .payments{
        .row{
            gap: 16px;
            a{
                flex-basis: 45%;
                display: flex;
                justify-content: center;
            }
        }
    }
}
</style>