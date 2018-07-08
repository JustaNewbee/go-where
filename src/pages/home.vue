<template>
    <div class="home-page">
        <go-header></go-header>
        <swiper></swiper>
        <icon-list></icon-list>
        <recommand-list></recommand-list>
        <weekend-travel></weekend-travel>
    </div>
</template>

<script>
import Header from '@/components/Header'
import Swiper from '@/components/Swiper'
import IconList from '@/components/IconList'
import Recommand from '@/components/Recommand'
import WeekendTravel from '@/components/WeekendTravel'
export default {
    name: 'Home',
    components: {
        goHeader: Header,
        swiper: Swiper,
        iconList: IconList,
        recommandList: Recommand,
        weekendTravel: WeekendTravel
    }
}
</script>

<style>

</style>
