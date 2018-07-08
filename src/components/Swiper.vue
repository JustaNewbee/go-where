<template>
    <swiper :options="swiperOption" class='swiper' v-if="showSwiper">
        <!-- slides -->
        <swiper-slide v-for="item of list" :key="item.imgId">
           <img class="swiper-img" :src="item.imgUrl" alt="去哪儿门票">
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
</template>

<script>
// import 'swiper/dist/css/swiper.css'
// import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
    name: 'carrousel',
    props: {
        list: Array
    },
    data () {
        return {
            swiperOption: {
                pagination: '.swiper-pagination',
                loop: true
            }
        }
    },
    computed: {
        showSwiper () {
            return this.list.length
        }
    }
}
</script>

<style lang="scss">
    .swiper {
        width: 100%;
        height: 0;
        padding-bottom: 26.667%;
        background: $load-bg-color;
        .swiper-img {
            display: block;
            width: 100%;
        }
        .swiper-pagination-bullet-active {
            background-color: $color-white;
        }
    }
</style>
