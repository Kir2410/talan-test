<template>
    <div class="container">
        <div class="banner">
            <div class="banner__content">
                <img src="../assets/operator.png" alt="">
                <div class="content__text">
                    <h4>Нужна консультация?</h4>
                    <span>Оставьте номер телефона – наши специалисты свяжутся с вами и оперативно ответят на любой вопрос</span>
                </div>
            </div>
            <input type="text" name="" id="" placeholder="Имя">
            <input type="text" name="" id="" placeholder="Телефон">
            <button
                @click="$emit('showModal')"
            >
                Заказть звонок
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name: "Banner"
}
</script>

<style lang="scss" scoped>
@import "@/styles/_variables.scss";

.container {
    margin: 60px auto;
}

.banner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 138px;
    width: 100%;
    border-radius: 24px;
    background: $main-color;
    padding: 19px 40px;

    &__content {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 465px;

        & img {
            margin-right: 26px;
        }
    }
}


.content__text {
    font-family: 'Stolzl-Medium';
    font-size: 21px;
    line-height: 25px;
    color: $background;

    & span {
        width: 339px;
        font-family: 'GraphikLCG-Regular';
        font-size: 12px;
        line-height: 18px;
    }
}
input {
    width: 230px;
    height: 34px;
    background: $background;
    border: none;
    border-radius: 12px;
    padding: 6px 12px 4px;
    font-family: 'GraphikLCGRegular';
    font-size: 14px;
    line-height: 24px;
    color: $text-input-color;
    &:focus {
        box-shadow: inset 0 1px 4px rgba(0,0,0,0.25);
        outline: none;
    }
}

button {
    width: 200px;
    height: 34px;
    background: $main-dark-color;
    border: none;
    border-radius: 12px;
    padding: 11px;
    font-family: 'Stolzl-Bold';
    font-size: 10px;
    line-height: 12px;
    text-align: center;
    letter-spacing: 0.1em;
    color: $background;
    text-transform: uppercase;
    cursor: pointer;

    &:hover {
        opacity: .7;
    }
}
</style>