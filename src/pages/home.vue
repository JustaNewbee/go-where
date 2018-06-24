<template>
    <div class="home-page">
        <go-header/>
        <swiper/>
        <icon-list/>
    </div>
</template>

<script>
import Header from '@/components/Header'
import Swiper from '@/components/Swiper'
import IconList from '@/components/IconList'
export default {
    name: 'Home',
    components: {
        goHeader: Header,
        swiper: Swiper,
        iconList: IconList
    }
}
</script>

<style scoped>

</style>
