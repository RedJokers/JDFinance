<template lang="html">
    <div>
        <Header/>
        <HSlider/>
        <Novice/>
        <Borrow/>
        <Money/>
        <Product/>
        <Life/>
        <Footer/>
    </div>
</template>

<script>
import Header from "../public/header.vue"
import Footer from "../public/footer.vue"
import HSlider from "./hslider.vue"
import Novice from "./novice.vue"
import Borrow from "./borrow.vue"
import Money from "./money.vue"
import Product from "./product.vue"
import Life from "./life.vue"
export default {
    components: {
        Header,
        HSlider,
        Novice,
        Borrow,
        Money,
        Product,
        Life,
        Footer,
    },
}
</script>

<style lang="scss" module>

</style>
