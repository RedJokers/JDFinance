<template lang="html">
    <div>
        <Header/>
        <Mslider/>
        <Ada/>
        <Money/>
        <Adb/>
        <Footer/>
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
export default {
    components: {
        Header,
        Footer,
        Nvbar,
        Mslider,
        Ada,
        Money,
        Adb,
    },
}
</script>

<style lang="scss" module>

</style>
