<template>
    <div class="weekend-travel">
        <h2>周末去哪儿</h2>
        <ul class="weekend-travel-list">
            <li v-for="item of list" :key="item.travel_id">
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
    props: {
        list: Array
    }
}
</script>

<style lang="scss">
    .weekend-travel {
        h2 {
            padding: 0 .3rem;
            margin-bottom: .4rem;
        }
        .item-img-wrapper {
            height: 0;
            padding-bottom: 37.09%;
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
