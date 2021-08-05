<template>
    <div class="contact">
        <div class="container">
            <h2 class="title">Остались вопросы? Готовы ответить!</h2>
            <form action="">
                <input type="text" name="" id="" placeholder="Ваше имя">
                <input type="tel" name="" id="" placeholder="Ваши контакты">
                <input type="email" name="" id="" placeholder="Ваши е-мейл">
                <button type="submit" class="btn">написать нам</button>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    name : "Contact",
}
</script>

<style lang="scss">
.contact{
    position: relative;
    background-image: url('../assets/images/bgFooter.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    padding: 320px 0;
    .title{
        color: white;
    }
    form{
        margin: 40px 0;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        gap: 30px;
        input{
            width: 80%;
            padding: 28px;
            background: #FFFFFF;
            border-radius: 50px;
            border: none;
            outline: none;
            font-weight: 400;
            font-size: 20px;
            line-height: 24px;
            color: rgba(126, 126, 126, 0.5);
            &::placeholder{
                font-weight: 400;
                font-size: 20px;
                line-height: 24px;
                color: rgba(126, 126, 126, 0.5);
            }
        }
    }
    .btn{
        margin-top: 12px;
        background: transparent;
        border-color: white;
        color: white;
        border-width: 1px;
    }
}

@media (max-width:500px) {
    .contact{
         form {
             input{
                width: 92%;
                padding: 24px;
             }
             .btn{
                padding: 16px 16px;
                font-size: 16px;
                width: 60%;
             }
         }
    }
}
</style>