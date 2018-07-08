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
    props: {
        list: Array
    },
    data () {
        return {
            swiperOption: {

            }
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
            this.list.forEach((item, index) => {
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

<style lang="scss">
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
