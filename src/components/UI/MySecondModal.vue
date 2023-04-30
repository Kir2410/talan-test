<template>
    <div class="modal" v-if="show" @click="hideModal">
        <div class="modal__content" @click.stop>
            <h2 class="modal__title">Заявка отправлена</h2>
            <div class="modal__operator">
                <img src="../../assets/operator.png" class="modal__image">
                <div class="modal__text">
                    <p class="modal__message">«Перезвоню вам в самое ближайшее время»</p>
                    <div class="modal__contacts">
                        <span>Менеджер по продажам</span>
                        <span>Анна Корнеева</span>
                        <span>+7 905 875 64 32</span>
                    </div>
                </div>
            </div>
            <button class="modal__button" @click="hideModal">Закрыть</button>
            <img src="../../assets/close_button.png"  class="modal__close" @click="hideModal"/>
        </div>
    </div>
</template>

<script>
export default {
    name: "MySecondModal",
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
    }

    &__operator {
        display: flex;
        align-items: start;
        justify-content: start;
        margin: 62px 0 79px;
    }


    &__image {
        margin-right: 16px;
    }

    &__text {
        padding-top: 26px;
        font-family: 'GraphikLCGRegular';
        font-size: 16px;
        line-height: 24px;
        letter-spacing: 0.156765px;
        color: $text-dark-color;
    }

    &__message {

    }

    &__contacts {
        margin-top: 18px;
        display: flex;
        align-items: start;
        justify-content: start;
        flex-direction: column;
        font-family: 'GraphikLCGRegular';
        font-size: 14px;
        line-height: 19px;
        letter-spacing: 0.156765px;
        color: $text-footer-color;

        & span:not(:last-child) {
            display: block;
        }
    }

    &__button {
        width: 100%;
        height: 34px;
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