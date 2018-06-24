<template>
    <swiper class="icon-list" :options="swiperOption">
        <swiper-slide v-for="(page, index) of pages" :key="index">
            <div class="icon-list-item" v-for="item of page" :key="item.iconId">
                <div class="icon">
                    <img :src="item.iconUrl">
                </div>
                <p>{{item.iconName}}</p>
            </div>
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
</template>

<script>
export default {
    name: 'IconList',
    data () {
        return {
            swiperOption: {

            },
            iconList: [
                {
                    iconId: '01',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                    iconName: '景点门票'
                },
                {
                    iconId: '02',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
                    iconName: '水上玩乐'
                },
                {
                    iconId: '03',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
                    iconName: '游乐场'
                },
                {
                    iconId: '04',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
                    iconName: '自然风光'
                },
                {
                    iconId: '05',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                    iconName: '一日游'
                },
                {
                    iconId: '06',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
                    iconName: '福州必游'
                },
                {
                    iconId: '07',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
                    iconName: '武夷山'
                },
                {
                    iconId: '08',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
                    iconName: '海洋馆'
                },
                {
                    iconId: '09',
                    iconUrl: 'http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png',
                    iconName: '水上玩乐'
                }
            ]
        }
    },
    computed: {
        // pages () {
        //     const pages = []
        //     for (let i = 0; i < this.iconList.length; i++) {
        //         const page = Math.floor(i / 8)
        //         if (!pages[page]) {
        //             pages[page] = []
        //         }
        //         //console.log(this.iconList[i])
        //         pages[page].push(this.iconList[i])
        //     }
        //     return pages
        // }
        // es6 method
        pages () {
            const pages = []
            this.iconList.forEach((item, index) => {
                const page = Math.floor(index / 8)
                if (!pages[page]) {
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages
        }
    }
}
</script>

<style lang="scss" scoped>
    .icon-list {
        &-item {
            float: left;
            width: 25%;
            padding-top: .2rem;
            text-align: center;
            .icon {
                height: 0;
                padding-bottom: 60%;
                margin-bottom: .2rem;
                img {
                    width: 60%;
                }
            }
            p {
                font-size: .3rem;
                @include textOverflow();
            }
        }
    }
</style>
