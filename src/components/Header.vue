<template>
    <header class="header">
        <div class="container">
            <div class="header__company">
                <img src="@/assets/logo.png" alt="">
                <DropdownItem>Ижевск</DropdownItem>
            </div>
            <div class="header__about">
                <DropdownItem>Объекты</DropdownItem>
                <DropdownItem>О компании</DropdownItem>
            </div>
            <div class="header__user">
                <div>
                    <div>+7 3412 918-742</div>
                    <div class="time">с 9:00 до 19:00</div>
                </div>
                <div>
                    <img src="../assets/profile.png" alt="">
                    Корзина
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
@import "@/styles/_variables.scss";

.header {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 70px;
    color: $main-color;
    font-family: Stolzl-Bold;
    font-size: 12px;
    line-height: 14px;
    letter-spacing: 0.1em;
    text-transform: uppercase;

    &__company {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 122px;

        & img {
            cursor: pointer;
        }
    }

    &__about {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 252px;
        height: 100%;
    }

    &__user {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 328px;
    }
}

.time {
    margin-top: 7px;
    font-family: 'GraphikLCGRegular';
    font-size: 10px;
    line-height: 10px;
    color: $qwertyui;
}
</style>
<script>
import DropdownItem from "@/components/UI/DropdownItem";
export default {
    name: "Header",
    components: {DropdownItem}
}
</script>