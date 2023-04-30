<template>
    <Header/>
    <Apartment/>
    <Banner @showModal="showModal"/>
    <Footer @showModal="showModal"/>
    <MyModal v-model:show="modalVisible" @showSecondModal="showSecondModal"/>
    <MySecondModal v-model:show="secondModalVisible"/>
</template>

<style lang="scss">
@import "@/styles/_fonts.scss";

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.container {
    width: 1360px;
    margin: 20px auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

@media screen and (max-width:1440px) {
    .container {
        width: 1200px;
    }
}

@media screen and (max-width:1280px) {
    .container {
        width: 984px;
    }
}

@media screen and (max-width:1024px) {
    .container {
        width: 800px;
    }
}

</style>
<script>
import Header from "@/components/Header";
import Footer from "@/components/Footer";
import Banner from "@/components/Banner";
import Apartment from "@/components/Apartment";
import MyModal from "@/components/UI/MyModal";
import MySecondModal from "@/components/UI/MySecondModal";

export default {
    components: {MySecondModal, MyModal, Apartment, Banner, Footer, Header},
    data() {
        return {
            modalVisible: false,
            secondModalVisible: false
        }
    },
    methods: {
        showModal() {
            this.modalVisible = true
        },
        showSecondModal() {
            this.modalVisible = false
            this.secondModalVisible = true
        }
    }
}
</script>