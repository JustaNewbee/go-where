<template>
    <div class="weekend-travel">
        <h2>周末去哪儿</h2>
        <ul class="weekend-travel-list">
            <li v-for="item of travel_list" :key="item.travel_id">
                <a href="#">
                    <div class="item-img-wrapper">
                        <img :src="item.travel_img" alt="weekend travel img">
                    </div>
                    <div class="item-detail">
                        <p class="title">{{item.travel_title}}</p>
                        <p class="desc">{{item.travel_desc}}</p>
                    </div>
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'WeekendTravel',
    data () {
        return {
            travel_list: [
                {
                    travel_id: '001',
                    travel_title: '福州必游TOP10',
                    travel_desc: '大美福州，必游之处',
                    travel_img: 'http://img1.qunarzz.com/sight/source/1505/68/de862f94e383a6.jpg_r_640x214_f9df927b.jpg'
                }
            ]
        }
    }
}
</script>

<style lang="scss">
    .weekend-travel {

        h2 {
            padding: .3rem .3rem 0;
            margin-bottom: .4rem;
        }
        .item-img-wrapper {
            img {
                display: block;
                width: 100%;
            }
        }
        .item-detail {
            padding: .2rem .3rem;
            color: $color-dark;
            .title {
                font-size: .28rem;
                margin-bottom: .2rem;
                @include textOverflow();
            }
            .desc {
                font-size: .24rem;
                color: $color-gray-dark;
                @include textOverflow();
            }
        }
    }
</style>
