<template>
    <swiper :options="swiperOption" class='swiper'>
        <!-- slides -->
        <swiper-slide v-for="item of swiperList" :key="item.imgId">
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
    data () {
        return {
            swiperOption: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [
                {
                    imgId: '01',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/df/70f59ca5c4ab2d02.jpg_750x200_4d026109.jpg'
                },
                {
                    imgId: '02',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/c5/8f384b861e4e9e02.jpg_750x200_29d574ba.jpg'
                },
                {
                    imgId: '03',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/fc/e47aa3e1c67bbc02.jpg_750x200_0f3eecf8.jpg'
                },
                {
                    imgId: '04',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/f2/91b285a08ee21c02.jpg_750x200_8a73fd08.jpg'
                },
                {
                    imgId: '05',
                    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1609/7f/c0cdf389bebe9702.jpg_750x200_973ef1e6.jpg'
                }
            ]
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
