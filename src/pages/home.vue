<template>
    <div class="home-page">
        <go-header/>
        <swiper/>
        <icon-list/>
        <recommand-list/>
    </div>
</template>

<script>
import Header from '@/components/Header'
import Swiper from '@/components/Swiper'
import IconList from '@/components/IconList'
import Recommand from '@/components/Recommand'
export default {
    name: 'Home',
    components: {
        goHeader: Header,
        swiper: Swiper,
        iconList: IconList,
        recommandList: Recommand
    }
}
</script>

<style>

</style>
