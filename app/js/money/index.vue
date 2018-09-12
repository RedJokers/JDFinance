<template lang="html">
    <div>
        <Header/>
        <Mslider/>
        <Ada/>
        <Money/>
        <Adb/>
        <Finance/>
        <Adc/>
        <Footer cname="cname"/>
        <Nvbar/>
    </div>
</template>

<script>
import Header from "../public/header.vue"
import Footer from "../public/footer.vue"
import Nvbar from "../public/navbar.vue"
import Mslider from "./mslider.vue"
import Ada from "./ada.vue"
import Money from "./money.vue"
import Adb from "./adb.vue"
import Finance from "./finance.vue"
import Adc from "./adc.vue"
export default {
    components: {
        Header,
        Footer,
        Nvbar,
        Mslider,
        Ada,
        Money,
        Adb,
        Finance,
        Adc,
    },
}
</script>

<style lang="scss">
    .cname {
        li:first-child {
            display: none;
        }
    }
</style>
