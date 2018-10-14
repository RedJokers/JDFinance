<template lang="html">
    <div>
        <Header/>
        <Daily/>
        <In/>
        <More/>
        <Footer/>
        <Nvbar/>
    </div>
</template>

<script>
import Header from "../public/header.vue"
import Footer from "../public/footer.vue"
import Nvbar from "../public/navbar.vue"
import Daily from "./daily.vue"
import In from "./in.vue"
import More from "./more.vue"
export default {
    components: {
        Header,
        Footer,
        Nvbar,
        Daily,
        In,
        More,
    },
}
</script>

<style lang="scss">

</style>
