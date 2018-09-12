<template lang="html">
    <div>
        <Header/>
        <Islider/>
        <Welfare/>
        <Service/>
        <Footer/>
        <Nvbar/>
    </div>
</template>

<script>
import Header from "../public/header.vue"
import Footer from "../public/footer.vue"
import Nvbar from "../public/navbar.vue"
import Islider from "./islider.vue"
import Welfare from "./welfare.vue"
import Service from "./service.vue"
export default {
    components: {
        Header,
        Footer,
        Nvbar,
        Islider,
        Welfare,
        Service,
    },
}
</script>

<style lang="scss">

</style>
