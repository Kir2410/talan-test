<template>
    <footer class="footer">
        <div class="container footer__container">
            <hr width="100%" color="#DFDFDF">
            <div class="footer__top">
                <div class="footer__column towns">
                    <h4>Города</h4>
                    <ul>
                        <li v-for="town in towns">{{town.title}}</li>
                    </ul>
                </div>
                <div class="footer__column about">
                    <h4>О компании</h4>
                    <ul>
                        <li v-for="link in  aboutLinks">{{link.title}}</li>
                    </ul>
                </div>
                <div class="footer__column partners">
                    <h4>Партнерам</h4>
                    <ul>
                        <li v-for="link in  partnersLinks">{{link.title}}</li>
                    </ul>
                </div>
                <div class="footer__column contacts">
                    <h4>Контакты</h4>
                    <div class="contacts__address">
                        <span>Отдел продаж:</span>
                        <span>ул. Красноармейская, 86</span>
                    </div>
                    <div class="contacts__phone">
                        <div>+7 3412 918-742</div>
                        <div class="contacts__time">с 9:00 до 19:00</div>
                    </div>
                    <button
                        @click="$emit('showModal')"
                    >
                        Заказать звонок
                    </button>
                </div>
                <div class="footer__column download">
                    <h4>Приложение Талан</h4>
                    <a href="">
                        <img src="../assets/app.png" alt="">
                    </a>
                </div>
            </div>
            <div class="footer__bottom">
                <div class="bottom__about">
                    <span class="bottom__team">© 2019 Талан</span>
                    <div class="bottom__links">
                        <a href="#">Гарантийные замечания</a>
                        <a href="#">Соглашение и политика по обработке персональных данных</a>
                    </div>
                </div>
                <p class="bottom__public">
                    Обращаем внимание, что настоящий рекламный материал носит исключительно информационный характер
                    и не является публичной офертой, определяемой положениями статьи 437 Гражданского кодекса РФ.<br/>
                    Общество с ограниченной ответственностью «ТАЛАН-ФИНАНС» (ОГРН 1117746313739) публикует информацию,
                    подлежащую раскрытию эмитентами эмиссионных ценных бумаг, на странице в сети Интернет, предоставленной
                    распространителем информации на рынке ценных бумаг ООО «Интерфакс-ЦРКИ», аккредитованным ЦБ РФ
                    на раскрытие информации, по адресу: http://www.e-disclosure.ru/portal/company.aspx?id=37631
                </p>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@import "@/styles/_variables.scss";

.footer__container {
    display: flex;
    align-items: start;
    justify-content: space-between;
    flex-direction: column;
}

.footer {
    &__top, .footer__bottom {
        width: 100%;
        display: flex;
        align-items: start;
        justify-content: space-between;
    }

    &__top {
        margin-top: 40px;
    }

    &__bottom {
        margin: 58px 0 38px;
    }

    &__column {
        width: 15%;
        display: flex;
        align-items: start;
        justify-content: start;
        flex-direction: column;


        & h4 {
            font-family: 'Stolzl-Bold';
            font-size: 12px;
            line-height: 14px;
            letter-spacing: 0.1em;
            color: $text-color;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        & li {
            cursor: pointer;

            &:hover {
                opacity: .7;
            }
        }
    }
}

.towns {
    width: 32%;

    & ul {
        width: 100%;
        display: grid;
        grid-auto-flow: column;
        grid-template-rows: repeat(8, 1fr);
        font-family: 'GraphikLCGMedium';
        font-size: 12px;
        line-height: 26px;
        color: $main-color;
        list-style-type: none;
    }
}

.about {
    & ul {
        width: 100%;
        display: grid;
        grid-auto-flow: column;
        grid-template-rows: repeat(8, 1fr);
        font-family: 'GraphikLCGMedium';
        font-size: 12px;
        line-height: 26px;
        color: $main-color;
        list-style-type: none;
    }
}

.partners {
    & ul {
        width: 100%;
        display: grid;
        grid-auto-flow: column;
        grid-template-rows: repeat(8, 1fr);
        font-family: 'GraphikLCGMedium';
        font-size: 12px;
        line-height: 26px;
        color: $main-color;
        list-style-type: none;
    }
}

.contacts {
    &__address {
        font-family: 'GraphikLCGRegular';
        font-size: 10px;
        line-height: 22px;
        color: $qwertyui;

        & span {
            display: block;

            &:last-child {
                font-family: 'GraphikLCGMedium';
                font-size: 12px;
                line-height: 22px;
                color: $text-color;
            }
        }
    }

    &__phone {
        margin-top: 4px;
        color: $main-color;
        font-family: Stolzl-Bold;
        font-size: 12px;
        line-height: 14px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
    }

    &__time {
        margin-top: 7px;
        font-family: 'GraphikLCGRegular';
        font-size: 10px;
        line-height: 10px;
        color: $qwertyui;
    }

    button {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 149px;
        height: 30px;
        margin-top: 22px;
        background: $background;
        box-shadow: 0px 2px 10px rgba(186, 189, 191, 0.42);
        border-radius: 12px;
        border: none;
        font-family: 'Stolzl-Bold';
        font-size: 10px;
        line-height: 12px;
        letter-spacing: 0.1em;
        color: $main-color;
        cursor: pointer;

        &:hover {
            color: $background;
            background: $main-color;
            opacity: .7;
        }
    }
}

.download {
    & h4 {
        margin-bottom: 23px;
    }
}

.bottom {
    &__about {
        display: flex;
        align-items: start;
        justify-content: start;
        flex-direction: column;
    }

    &__team {
        display: block;
        font-family: 'GraphikLCGMedium';
        font-size: 12px;
        line-height: 12px;
        color: $text-footer-color;
    }

    &__links {
        display: flex;
        align-items: start;
        justify-content: start;
        flex-direction: column;
        margin-top: 24px;

        & a {
            text-decoration: none;
            font-family: 'GraphikLCGMedium';
            font-size: 12px;
            line-height: 12px;
            color: $main-color;

            &:not(:last-child) {
                margin-bottom: 6px;
            }

            &:hover {
                opacity: .7;
            }
        }
    }

    &__public {
        display: block;
        width: 890px;
        font-family: 'GraphikLCGRegular';
        font-size: 12px;
        line-height: 18px;
        color: $text-footer-color;
    }
}
</style>

<script>
export default {
    name: "Footer",
    data() {
        return {
            towns: [
                {id: 1, title: 'Ижевск', url: ''},
                {id: 2, title: 'Уфа', url: ''},
                {id: 3, title: 'Пермь', url: ''},
                {id: 4, title: 'Набережные Челны', url: ''},
                {id: 5, title: 'Тюмень', url: ''},
                {id: 6, title: 'Хабаровск', url: ''},
                {id: 7, title: 'Сочи', url: ''},
                {id: 8, title: 'Тверь', url: ''},
                {id: 9, title: 'Ханты-Мансийск', url: ''},
                {id: 10, title: 'Нижний Новгород', url: ''},
                {id: 11, title: 'Новосибирск', url: ''},
                {id: 12, title: 'Нижневартовск', url: ''},
                {id: 13, title: 'Владивосток', url: ''},
                {id: 14, title: 'Севастополь', url: ''},
                {id: 15, title: 'Ярославль', url: ''}
            ],
            aboutLinks: [
                {id: 1, title: 'Контакты', url: ''},
                {id: 2, title: 'Команда', url: ''},
                {id: 3, title: 'Вакансии', url: ''},
                {id: 4, title: 'Миссия компании', url: ''},
                {id: 5, title: 'Новости', url: ''},
                {id: 6, title: 'Открытые данные', url: ''},
                {id: 7, title: 'Карьера', url: ''},
                {id: 8, title: 'Талан.журнал', url: ''}
            ],
            partnersLinks: [
                {id: 1, title: 'Риелторам', url: ''},
                {id: 2, title: 'Владельцам участков', url: ''},
                {id: 3, title: 'Тендеры', url: ''},
                {id: 4, title: 'Талан.инвест', url: ''}
            ]
        }
    }
}

</script>

