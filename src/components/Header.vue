<template>
    <header class="header">
        <div class="container">
            <div class="row">
                <a href="/" class="logo">
                    <img src="../assets/logo.png" alt="">
                </a>
                <nav class="navbar">
                    <div class="row">
                        <div class="header__pages">
                            <router-link to="/" class="header__page">вебмастерам</router-link>
                            <router-link to="/" class="header__page">рекламодателям</router-link>
                        </div>
                        <button class="loginBtn desktop">вход  |  регистрация</button>
                        <button class="loginBtn mobile">вход</button>
                        <div class="lang">
                            <input type="radio" name="lang" id="uz">
                            <label for="uz">uz</label>
                            <input checked type="radio" name="lang" id="rus">
                            <label  for="rus">rus</label>
                        </div>
                    </div>
                </nav>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name : "Header",
}
</script>

<style lang="scss">
.header{
    padding: 16px 0;
    background: white;
    z-index: 2;
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    &__pages{
        display: flex;
        gap: 48px;
        padding: 0 50px;
        border-right: 1px solid #F4F4F4;
        height: 54px;
        align-items: center;
    }
    &__page{
        font-weight: bold;
        font-size: 13px;
        line-height: 16px;
        text-transform: uppercase;
        color: #565656;
    }
    .row{
        justify-content: space-between;
    }
    .lang{
        margin: 0 28px;
        width: 84px;
        height: 36px;
        display: flex;
        background: #F9F9F9;
        border: 1px solid #EBEBEB;
        box-sizing: border-box;
        border-radius: 24px;
        justify-content: space-between;
        input{
            display: none;
        }
        label{
            height: 100%;
            flex-basis: 50%;
            line-height: 32px;
            text-align: center;
            font-weight: bold;
            font-size: 14px;
            color: #919191;
        }
        input:checked + label{
            background: #4EAAE0;
            border-radius: 24px;
            flex-basis: 60%;
            color: white;
            transition-timing-function: ease-in;
            transition: 0.4s;
            transform-origin: left;
        }
        
    }
}
.loginBtn{
    font-weight: 800;
    font-size: 13px;
    line-height: 16px;
    text-transform: uppercase;
    color: #55B570;
    background: transparent;
    border: none;
    outline: none;
    padding: 0 50px;
    border-right: 1px solid #F4F4F4;
    height: 54px;
}
.mobile{
    display: none;
}
.logo{
    width: 110px;
    height: 50px;
    display: block;
}

@media(max-width:776px){
    .mobile{
        display: block;
    }
    .desktop{
        display: none;
    }

    .header{
        box-shadow: 0px 10px 10px rgba(0, 0, 0, 0.05);
        &__pages{
            display: none;
        }
        .lang{
            margin: 0 16px;
        }

    }
    .logo{
        width: 78px;
    }
    .loginBtn{
        padding: 0 16px;
        height: 36px;
    }
}
</style>