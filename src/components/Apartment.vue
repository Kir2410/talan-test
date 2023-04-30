<template>
    <div class="container">
        <div class="apartment">
            <div class="apartment__title">
                <h2>3-комнатная квартира Евро+ с 2 гардеробными и мастер-спальней и теплой видовой лаундж-лоджией</h2>
                <div class="title__percent">
                    <div class="title__ready">
                        <div class="title__ellipse"></div>
                        <img src="../assets/ready.png" alt="">
                        <span>83%</span>
                    </div>
                    <div class="title__date">
                        Октябрь 2020
                    </div>
                </div>
            </div>
            <div class="apartment__container">
                <div class="apartment__slider">
                    <img src="../assets/plan1.png" alt="">
                </div>
                <div class="apartment__about">
                    <div class="about__cost">
                        от 2 305 800 ₽
                        <span> 52 468 ₽/м<sup>2</sup></span>
                    </div>
                    <div class="about__favorites">
                        <img src="../assets/heart.png" alt="">
                        <span>в избранное</span>
                        <span class="about__favorites_info">
                            32 человека добавили в избранное
                        </span>
                    </div>
                    <div class="about__parameters">
                        <div class="about__parameter" v-for="parameter in parameters">
                            <span>{{parameter.title}}</span>
                            <span>{{parameter.value}}</span>
                        </div>
                    </div>
                    <div class="about__payment">
                        <div class="payment__mortgage">
                            <div class="payment__title">Ипотека: от 9,2%</div>
                            <div class="payment__value">20 380 ₽/месяц </div>
                        </div>
                        <div class="payment__credit">
                            <div class="payment__title">Рассрочка: 0%</div>
                            <div class="payment__value">20 380 ₽/месяц </div>
                        </div>
                    </div>
                    <button class="about__button">
                        Добавить в корзину
                    </button>
                    <div class="about__description">
                        <h3>Подробнее о квартире</h3>
                        <p>
                            Просторная мастер-спальня 15 м<sup>2</sup> с собственной простороной гардеробной 2 м<sup>2</sup> и собственной теплой витражной лаундж-лоджией
                            с французским балконом. Высаживайте любимые цветы, наслаждайтесь закатами и заряжайтесь хорошим настроением
                            с самого утра.
                        </p>
                        <p>
                            Удобное разделение на гостевую и приватную зоны – из коридора мы попадаем прямо в столовую
                        </p>
                        <p>
                            Парадная гостиная-столовая 18 м<sup>2</sup> с двумя окнами и местом под большой шкаф или домашнюю библиотеку
                        </p>
                        <p>
                            Просторная ванная комната 5,1 м<sup>2</sup>
                        </p>
                        <p>
                            2 отдельные гардеробные
                        </p>
                    </div>
                    <div class="about__emoji">
                        <h3>Оцените планировку</h3>
                        <div class="emoji__rating">
                            <img src="../assets/emo-1.svg" alt="">
                            <img src="../assets/emo-2.svg" alt="">
                            <img src="../assets/emo-3.svg" alt="">
                            <img src="../assets/emo-4.svg" alt="">
                            <img src="../assets/emo-5.svg" alt="">
                        </div>
                    </div>
                    <div class="about__similar">
                        <h3>Похожие квартиры</h3>
                        <div class="similar__apartments">
                            <div class="similar__apartment">
                                <img src="../assets/plan-mini.png" alt="" class="similar__image">
                                <div class="similar__description">
                                    <img src="../assets/dark_heart.png" alt="" class="similar__like">
                                    <div class="similar__price">
                                        3 640 000 ₽
                                    </div>
                                    <div class="similar__parameters">
                                        <span>3-комн.</span>
                                        <span>4/14 этаж</span>
                                        <span>102 м²</span>
                                    </div>
                                    <div class="similar__building">ЖК «Фруктовая»</div>
                                </div>
                            </div>
                            <div class="similar__apartment">
                                <img src="../assets/plan-mini.png" alt="" class="similar__image">
                                <div class="similar__description">
                                    <img src="../assets/dark_heart.png" alt="" class="similar__like">
                                    <div class="similar__price">
                                        3 640 000 ₽
                                    </div>
                                    <div class="similar__parameters">
                                        <span>3-комн.</span>
                                        <span>4/14 этаж</span>
                                        <span>102 м²</span>
                                    </div>
                                    <div class="similar__building">ЖК «Фруктовая»</div>
                                </div>
                            </div>
                            <div class="similar__apartment">
                                <img src="../assets/plan-mini.png" alt="" class="similar__image">
                                <div class="similar__description">
                                    <img src="../assets/dark_heart.png" alt="" class="similar__like">
                                    <div class="similar__price">
                                        3 640 000 ₽
                                    </div>
                                    <div class="similar__parameters">
                                        <span>3-комн.</span>
                                        <span>4/14 этаж</span>
                                        <span>102 м²</span>
                                    </div>
                                    <div class="similar__building">ЖК «Фруктовая»</div>
                                </div>
                            </div>
                            <div class="similar__apartment">
                                <img src="../assets/plan-mini.png" alt="" class="similar__image">
                                <div class="similar__description">
                                    <img src="../assets/dark_heart.png" alt="" class="similar__like">
                                    <div class="similar__price">
                                        3 640 000 ₽
                                    </div>
                                    <div class="similar__parameters">
                                        <span>3-комн.</span>
                                        <span>4/14 этаж</span>
                                        <span>102 м²</span>
                                    </div>
                                    <div class="similar__building">ЖК «Фруктовая»</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@import "@/styles/_variables.scss";

.container {
    margin-top: 100px;
}

.apartment {
    width: 100%;

    &__title {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;

        & h2 {
            width: 1200px;
            font-family: 'Stolzl-Bold';
            font-size: 36px;
            line-height: 43px;
            color: $text-color;
        }
     }

    &__container {
        margin-top: 30px;
        display: flex;
        align-items: start;
        justify-content: space-between;
    }

    &__slider {
        width: 660px;
        height: 580px;
        background: $background;
        box-shadow: 0 5px 13px rgba(186, 189, 191, 0.42);
        border-radius: 20px;
    }

    &__about {
        width: 660px;
    }
}

.title {
    &__percent {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 121px;
    }

    &__ellipse {
        position: absolute;
        width: 54px;
        height: 54px;
        border-radius: 50%;
        border: 2px solid rgba(24, 164, 82, 0.2);
    }

    &__ready {
        position: relative;
        margin-right: 13px;

        & span {
            display: block;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-family: 'Stolzl-Medium';
            font-size: 14px;
            line-height: 17px;
            color: #343434;
        }
    }

    &__date {
        width: 58px;
        font-family: 'GraphikLCGMedium';
        font-size: 14px;
        line-height: 20px;
        color: $main-color;
    }
}

.about {
    &__cost {
        font-family: 'GraphikLCGMedium';
        font-size: 42px;
        line-height: 42px;
        color: $text-color;

        & span {
            font-family: 'GraphikLCGRegular';
            font-size: 18px;
            line-height: 24px;
            letter-spacing: 0.156765px;
            color: $text-medium-color;
            margin-left: 24px;
        }
    }

    &__favorites {
        margin-top: 35px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 485px;
        font-family: 'Stolzl-Bold';
        font-size: 14px;
        line-height: 17px;
        letter-spacing: 0.12em;
        color: $main-color;
        text-transform: uppercase;

        &_info {
            font-family: 'GraphikLCGRegular';
            font-size: 18px;
            line-height: 24px;
            letter-spacing: 0.156765px;
            color: $text-medium-color;
            text-transform: none;
        }
    }

    &__parameters {
        margin-top: 32px;
        display: flex;
        align-items: center;
        justify-content: start;
        flex-direction: column;
    }

    &__parameter {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        font-family: 'GraphikLCGRegular';
        font-size: 16px;
        line-height: 20px;
        letter-spacing: 0.156765px;
        color: $text-medium-color;

        &:not(:last-child) {
            margin-bottom: 20px;
        }

        & span {
            display: block;
        }
    }

    &__payment {
        margin: 39px 0 40px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    &__button {
        margin-bottom: 56px;
        width: 660px;
        height: 48px;
        background: $main-color;
        border-radius: 12px;
        border: none;
        font-family: 'Stolzl-Bold';
        font-size: 16px;
        line-height: 19px;
        text-align: center;
        letter-spacing: 0.14em;
        color: #FFFFFF;
        text-transform: uppercase;
        cursor: pointer;

        &:hover {
            opacity: .7;
        }
    }

    &__description {

        & h3 {
            margin-bottom: 18px;
            font-family: 'Stolzl-Medium';
            font-size: 24px;
            line-height: 29px;
            color: $text-color;
        }

        & p {
            position: relative;
            margin-bottom: 22px;
            padding-left: 20px;
            font-family: 'GraphikLCGRegular';
            font-size: 16px;
            line-height: 24px;
            letter-spacing: 0.156765px;
            color: $text-dark-color;
            width: 583px;

            &:before {
                content: "";
                position: absolute;
                top: 7px;
                left: 0;
                height: 8px;
                width: 8px;
                background: $main-color;
                border-radius: 50%;
            }
        }
    }

    &__emoji {
        & h3 {
            margin-top: 46px;
            margin-bottom: 18px;
            font-family: 'Stolzl-Medium';
            font-size: 24px;
            line-height: 29px;
            color: $text-color;
        }
    }

    &__similar {
        & h3 {
            margin-top: 45px;
            margin-bottom: 18px;
            font-family: 'Stolzl-Medium';
            font-size: 24px;
            line-height: 29px;
            color: $text-color;
        }
    }
}

.emoji {
    &__rating {
        width: 313px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}

.similar {
    &__apartments {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 40px;
    }

    &__apartment {
        width: 310px;
        height: 140px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        background: $background;
        box-shadow: 0 5px 13px rgba(186, 189, 191, 0.42);
        border-radius: 20px;
        padding: 22px 20px 15px;
    }

    &__description {
        position: relative;
        padding: 7px 16px 0 0;
        display: flex;
        align-items: start;
        justify-content: space-between;
        flex-direction: column;
        width: 146px;
        height: 100%;
    }

    &__like {
        position: absolute;
        top: 0;
        right: 0;
    }

    &__price {
        font-family: 'GraphikLCGMedium';
        font-size: 15px;
        line-height: 15px;
        letter-spacing: 0.149292px;
        color: $text-dark-color;
    }

    &__parameters {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 9px;
        width: 133px;
        height: 35px;
        font-family: 'GraphikLCGRegular';
        font-size: 13px;
        line-height: 13px;
        letter-spacing: 0.156765px;
        color: #000000;
    }

    &__building {
        font-family: 'GraphikLCGRegular';
        font-size: 13px;
        line-height: 13px;
        letter-spacing: 0.156765px;
        color: #909DA8;
    }
}

.payment {
    &__mortgage {
        width: 50%;
        display: flex;
        align-items: start;
        justify-content: start;
        flex-direction: column;
        font-family: 'GraphikLCGMedium';
        font-size: 28px;
        line-height: 28px;
        color: $main-color;
        text-decoration-line: underline;
    }

    &__credit {
        width: 50%;
        display: flex;
        align-items: start;
        justify-content: start;
        flex-direction: column;
        font-family: 'GraphikLCGMedium';
        font-size: 28px;
        line-height: 28px;
        color: $text-color;
    }

    &__title {
        font-family: 'GraphikLCGRegular';
        font-size: 18px;
        line-height: 24px;
        letter-spacing: 0.156765px;
        color: $text-medium-color;
        margin-bottom: 12px;
    }
}

sup {
    line-height: 1;
}

@media screen and (max-width:1440px) {
    .apartment {
        &__title h2 {
            width: 80%;
            font-size: 32px;
        }

        &__slider, .apartment__about {
            width: 49%;
        }
    }

    .about {
        &__button {
            width: 100%;
        }
    }

    .similar {

        &__apartments {
            gap: 30px;
        }

        &__apartment {
            width: 100%;
        }
    }
}


</style>

<script>
export default {
    name: "Apartment",
    data() {
        return {
            parameters: [
                {id: 1, title: "Секция", value: 1},
                {id: 2, title: "Подъезд", value: 2},
                {id: 3, title: "Комнат", value: 3},
                {id: 4, title: "Этаж", value: "14 из 17"},
                {id: 5, title: "Общая площадь, м2", value: 46},
                {id: 6, title: "Жилая площадь, м2", value: 72}
            ]
        }
    }
}
</script>
