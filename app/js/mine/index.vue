<template>
    <section style="margin-top:120px">
        <nav-header/>
        <h2>//todo</h2>
        <nav-footer/>
        <nvbar/>
    </section>
</template>

<script>
import NavHeader from "../public/header.vue"
import NavFooter from "../public/footer.vue"
import Nvbar from "../public/navbar.vue"
export default {
    components: {
        NavHeader,
        Nvbar,
        NavFooter,
    },
}
</script>
