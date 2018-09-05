<template lang="html">
    <div>
        <Header/>
        <HSlider/>
        <Novice/>
        <Borrow/>
        <Money/>
    </div>
</template>

<script>
import Header from "../public/header.vue"
import HSlider from "./hslider.vue"
import Novice from "./novice.vue"
import Borrow from "./borrow.vue"
import Money from "./money.vue"
export default {
    components: {
        Header,
        HSlider,
        Novice,
        Borrow,
        Money,
    },
}
</script>

<style lang="scss" module>

</style>
