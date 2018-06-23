<template>
    <div class="home-page">
        <Header/>
        <Swiper/>
        <p>test</p>
    </div>
</template>

<script>
import Header from '@/components/Header'
import Swiper from '@/components/Swiper'
export default {
    name: 'Home',
    components: {
        Header,
        Swiper
    }
}
</script>

<style scoped>

</style>
