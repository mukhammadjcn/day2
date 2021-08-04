<template>
    <div class="intro">
        <div class="container">
            <h1 class="intro__title">Мобильная партнерская сеть</h1>
            <p class="info">Только рабочие офферы от прямых рекламодателей</p>
            <div class="scores">
                <span class="score">
                    <h2 class="score__value">300+</h2>
                    <p class="score__label">офферов по всему миру</p>
                </span>
                <hr>
                <span class="score">
                    <h2 class="score__value">70+</h2>
                    <p class="score__label">активных рекламодателей</p>
                </span>
                <hr>
                <span class="score">
                    <h2 class="score__value">6 лет</h2>
                    <p class="score__label">в аффилейт маркетинге</p>
                </span>
                <hr>
                <span class="score">
                    <h2 class="score__value">10.000+</h2>
                    <p class="score__label">конверсий в день</p>
                </span>
                
            </div>
            <div class="intro__options">
                <div class="intro__option">
                    <p class="minInfo">Я пользователь соцсетей, блогер, владелец сайта или арбитражник и хочу сотрудничать с топовыми мировыми брендами.</p>
                    <button class="intro__option-btn"><span>веб-мастерам</span> <svg width="10" height="20" viewBox="0 0 10 20" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M5.55301 19.7709C5.55324 19.7706 5.55352 19.7704 5.55375 19.7702L9.61625 15.688C9.92059 15.3821 9.91946 14.8875 9.6136 14.5831C9.30778 14.2787 8.81313 14.2799 8.50875 14.5857L5.78125 17.3265L5.78125 0.78125C5.78125 0.349765 5.43149 -1.92866e-07 5 -2.11727e-07C4.56852 -2.30588e-07 4.21875 0.349765 4.21875 0.78125L4.21875 17.3264L1.49125 14.5857C1.18688 14.2799 0.692228 14.2788 0.386407 14.5831C0.0805095 14.8875 0.0794547 15.3822 0.383751 15.688L4.44625 19.7702C4.44649 19.7704 4.44676 19.7706 4.44699 19.7709C4.75238 20.0769 5.24863 20.0759 5.55301 19.7709Z" fill="white"/></svg></button>
                </div>
                <hr>
                <div class="intro__option">
                    <p class="minInfo">Я пользователь соцсетей, блогер, владелец сайта или арбитражник и хочу сотрудничать с топовыми мировыми брендами.</p>
                    <button class="intro__option-btn green"><span>рекламодателю</span> <svg width="20" height="10" viewBox="0 0 20 10" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M19.7709 4.44699C19.7706 4.44676 19.7704 4.44648 19.7702 4.44625L15.688 0.383747C15.3821 0.0794115 14.8875 0.0805441 14.5831 0.386403C14.2787 0.692224 14.2799 1.18687 14.5857 1.49125L17.3265 4.21875H0.78125C0.349766 4.21875 0 4.56851 0 5C0 5.43148 0.349766 5.78125 0.78125 5.78125H17.3264L14.5857 8.50875C14.2799 8.81312 14.2788 9.30777 14.5831 9.61359C14.8875 9.91949 15.3822 9.92054 15.688 9.61625L19.7702 5.55375C19.7704 5.55351 19.7706 5.55324 19.7709 5.55301C20.0769 5.24762 20.0759 4.75137 19.7709 4.44699Z" fill="white"/></svg></button>
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
    name : "Intro",
    props : {
        option : {
            type : Object,
            default : () => {}
        }
    }
}
</script>

<style lang="scss">
.intro{
    background-image: url('../assets/images/bg.png');
    padding-top: 220px;
    padding-bottom: 64px;
    text-align: center;
    background-repeat: no-repeat;
    background-size: cover;
    &__title{
        font-weight: 900;
        font-size: 60px;
        line-height: 75px;
        text-transform: uppercase;
        color: #FFFFFF;
    }
    .info{
        padding: 16px 0 108px;
        color: white;
    }
    .scores{
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-wrap: wrap;
        hr{
            height: 120px;
            border-width: 0 2px 0 0;
            border-color: #F3F3F3;
            opacity: 0.8;
        }
        .score{
            flex-basis: 20%;
            padding: 24px 36px;
            &__value{
                font-weight: 800;
                font-size: 40px;
                line-height: 49px;
                text-align: center;
                color: #FFFFFF;
                margin-bottom: 12px;
            }
            &__label{
                font-weight: 500;
                font-size: 16px;
                line-height: 19px;
                text-align: center;
                color: #FFFFFF;
            }
        }
    }
    &__options{
        padding: 64px 48px;
        background: #FFFFFF;
        box-shadow: 0px 20px 80px rgba(0, 0, 0, 0.08);
        border-radius: 8px;
        display: flex;
        hr{
            border-width: 0 2px 0 0;
            border-color: #F3F3F3;
        }
    }
    &__option{

        .minInfo{
            margin-bottom: 24px;
            font-weight: 500;
            font-size: 16px;
            line-height: 24px;
            text-align: center;
            color: #000000;
        }
        &-btn{
            cursor: pointer;
            margin: auto;
            width: 60%;
            background: #2E9ADB;
            border-radius: 40px;
            padding: 28px 16px;
            border: none;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            transition: 0.2s cubic-bezier(0.075, 0.82, 0.165, 1);
            span{
                font-weight: 900;
                font-size: 20px;
                line-height: 24px;
                text-align: center;
                text-transform: uppercase;
                color: #FFFFFF;
            }
            svg{
                position: absolute;
                right: 36px;
                top: 50%;
                transform: translateY(-50%);
            }
        }
        &:nth-child(1) button{
            &:hover{
                box-shadow: 0px 10px 20px rgba(78, 170, 224, 0.35);
            }
        }
        .green{
            &:hover{
                box-shadow: 0px 10px 20px rgba(85, 181, 112, 0.35);
            }
        }
    }
}
.green{
    background: #55B570;
}

@media (max-width:776px) {
    .intro{
        padding-top: 164px;
        &__title{
            font-size: 32px;
            line-height: 40px;
        }
        .info{
            font-size: 16px;
            line-height: 19px;
            padding-bottom: 36px;
        }
        .scores{
            padding: 24px 0;
            gap: 24px;
            hr{
                display: none;
            }
            justify-content: center;
            .score{
                padding: 0;
                flex-basis: 40%;
                &__value{
                    font-size: 30px;
                    line-height: 37px;
                }
                &__label{
                    font-size: 13px;
                    line-height: 15px;
                }
            }
        }
        &__options{
            flex-direction: column;
            gap: 36px;
            padding: 24px;
            hr{
                border-width: 0 0 2px;
            }
        }
        
        
   
    }
}

@media(max-width:500px){
    .intro{
        &__options{
            padding: 24px 16px;
        }
        &__option-btn{
            width: 90%;
            padding: 20px;
            span{
                font-size: 16px;
                line-height: 24px;
                font-weight: 400;
            }
        }
        .green{
            svg{
                right: 18px;
            }
        }
    }
}
</style>