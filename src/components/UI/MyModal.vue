<template>
    <div class="modal" v-if="show" @click="hideModal">
        <div class="modal__content" @click.stop>
            <h2 class="modal__title">Заявка на бронирование</h2>
            <h3 class="modal__subtitle">Оставьте заявку на бронирование и наши специалисты свяжутся с вами в самое ближайшее время.</h3>
            <form action="">
                <input type="text" placeholder="Имя">
                <input type="text" placeholder="Телефон">
                <div class="modal__checkbox">
                    <input type="checkbox" id="personal_data">
                    <label for="personal_data">
                        <p>
                            Даю <a href="#">согласие</a> на обработку моих персональных данных,
                            с <a href="#">условиями политики</a> ознакомлен
                        </p>
                    </label>
                </div>
                <button class="modal__button" @click.prevent="$emit('showSecondModal')">Отправить заявку</button>
            </form>
            <img src="../../assets/close_button.png"  class="modal__close" @click="hideModal"/>
        </div>
        <MySecondModal/>
    </div>
</template>

<script>
export default {
    name: "MyModal",
    props: {
        show: {
            type: Boolean,
            default: false
        }
    },
    methods: {
        hideModal() {
            this.$emit('update:show', false)
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../../styles/_variables.scss";

.modal {
    position: fixed;
    display: flex;
    align-items: center;
    justify-content: center;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: rgba(0,0,0, .7);
    z-index: 2;

    &__content {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: start;
        flex-direction: column;
        margin: auto;
        padding: 60px 60px 47px;
        background: $background;
        width: 450px;
        height: 460px;
    }

    &__title {
        font-family: 'Stolzl-Medium';
        font-size: 24px;
        line-height: 29px;
        color: $text-color;
        margin-bottom: 30px;
    }

    &__subtitle {
        font-family: 'GraphikLCGRegular';
        font-size: 16px;
        line-height: 24px;
        letter-spacing: 0.156765px;
        color: $text-dark-color;
        margin-bottom: 10px;
    }

    & input[type="text"] {
        width: 334px;
        height: 34px;
        background: $background;
        border: 1px solid #E1E1E1;
        box-shadow: inset 0px 2px 5px rgba(0, 0, 0, 0.15);
        border-radius: 12px;
        padding: 6px 12px 4px;
        margin-top: 20px;
    }

    &__checkbox {
        margin-top: 22px;
        width: 100%;

        label {
             display: flex;
             align-items: start;
             justify-content: start;
             font-family: 'GraphikLCGRegular';
             font-size: 10px;
             line-height: 14px;
             color: $text-color;

            & p {
                padding-left: 6px;
            }

            & a {
                text-decoration: none;
                color: $main-color;
            }
         }

        & input {
            position: absolute;
            z-index: -1;
            opacity: 0;

            &+label::before {
                content: '';
                display: inline-block;
                width: 16px;
                height: 16px;
                flex-shrink: 0;
                flex-grow: 0;
                margin-right: 0.5em;
                border: 1px solid #E1E1E1;
                border-radius: 5px;
                background-repeat: no-repeat;
                background-position: center center;
                background-size: 15px 10px;
            }

            &:checked+label::before {
                background-image: url("../../assets/checked.png");
            }
        }
    }

    &__button {
        width: 100%;
        height: 34px;
        margin-top: 18px;
        background: $main-color;
        border-radius: 12px;
        border: none;
        font-family: 'Stolzl-Bold';
        font-size: 10px;
        line-height: 12px;
        text-align: center;
        letter-spacing: 0.14em;
        color: $background;
        text-transform: uppercase;
        cursor: pointer;

        &:hover {
            opacity: .7;
        }
    }

    &__close {
        position: absolute;
        top: 20px;
        right: 20px;
        cursor: pointer;

        &:hover {
            filter: brightness(70%);
        }
    }
}
</style>