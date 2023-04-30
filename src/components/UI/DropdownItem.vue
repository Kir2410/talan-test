<template>
    <div class="dropdown">
        <button class="dropdown__button">
            <slot></slot>
            <img src="../../assets/dropdown-arrow.png" alt="">
        </button>
        <div class="dropdown__content">
            <a href="#">Link 1</a>
            <a href="#">Link 2</a>
            <a href="#">Link 3</a>
        </div>
    </div>
</template>

<script>
export default {
    name: "DropdownItem"
}
</script>

<style lang="scss" scoped>
@import "../../styles/_variables.scss";

.dropdown {
    position: relative;
    display: inline-block;

    &__button {
        display: flex;
        align-items: center;
        background: transparent;
        color: $main-color;
        font-family: Stolzl-Bold;
        font-size: 12px;
        line-height: 14px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
        height: 100%;
        border: none;
        cursor: pointer;

        & img {
            margin-left: 7px;
        }
    }

    &__content {
        display: none;
        position: absolute;
        background-color: $background;
        min-width: 160px;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        z-index: 1;
        padding: 17px 0;

        & a {
            text-decoration: none;
            color: $main-color;
            font-family: Stolzl-Bold;
            font-size: 12px;
            line-height: 14px;
            letter-spacing: 0.1em;
            text-transform: uppercase;
            padding: 9px 33px 8px;
            display: block;

            &:hover {
                opacity: .7;
            }
        }
    }

    &:hover .dropdown__content {
        display: block;
    }

    &:hover .dropdown__button {
        opacity: .7;
    }
}
</style>