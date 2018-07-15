<template>
    <div class="home-page">
        <go-header :city="city"></go-header>
        <swiper :list="swiperList"></swiper>
        <icon-list :list="iconList"></icon-list>
        <recommand-list :list="recommandList"></recommand-list>
        <weekend-travel :list="travelList"></weekend-travel>
    </div>
</template>

<script>
import Header from '@/components/Header'
import Swiper from '@/components/Swiper'
import IconList from '@/components/IconList'
import Recommand from '@/components/Recommand'
import WeekendTravel from '@/components/WeekendTravel'
import axios from 'axios'
export default {
    name: 'Home',
    components: {
        goHeader: Header,
        swiper: Swiper,
        iconList: IconList,
        recommandList: Recommand,
        weekendTravel: WeekendTravel
    },
    data () {
        return {
            swiperList: [],
            iconList: [],
            recommandList: [],
            travelList: []
        }
    },
    methods: {
        getHomeData () {
            axios.get('/api/index.json').then(res => {
                let resData = res.data
                if (resData.ret && resData.data) {
                    this.city = resData.data.city
                    this.swiperList = resData.data.swiperList
                    this.iconList = resData.data.iconList
                    this.recommandList = resData.data.recommandList
                    this.travelList = resData.data.travelList
                }
            })
        }
    },
    created () {
        this.getHomeData()
    }
}
</script>

<style>

</style>
