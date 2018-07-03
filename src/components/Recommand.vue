<template>
    <div class="recommand">
        <h2 class="recommand-title">猜你喜欢</h2>
        <ul class="recommand-list">
            <li>
                <a href="">
                    <div class="item-img-wrapper">
                        <img src="http://img1.qunarzz.com/sight/p0/1707/45/4524631d448c1aea3.water.jpg_200x200_b7b204e1.jpg" alt="recommand img">
                    </div>
                    <div class="item-detail">
                        <p class="title">白水洋</p>
                        <p class="star">XXXXX</p>
                        <p class="money">
                            <span class="rmb">¥</span><span class="pay">38</span>起
                        </p>
                        <p class="address">屏南县</p>
                    </div>
                </a>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'recommand'
}
</script>

<style lang="scss">
    .recommand {
        padding: .3rem;
        .recommand-title {
            margin-bottom: .4rem;
        }
        .recommand-list {
            li a {
                display: flex;
                padding-bottom: 8px;
                border-bottom: 1px $color-gray-light-more solid;
                .item-img-wrapper {
                    flex: 0 1 2rem;
                    img {
                        display: block;
                        width: 100%;
                    }
                }
                .item-detail {
                    display: flex;
                    flex-direction: row;
                    flex-wrap: wrap;
                    flex: 1 1 auto;
                    align-items: center;
                    margin-left: 10px;
                    color: $color-dark;
                    .title {
                        flex: 1 1 100%;
                    }
                    .star {
                        flex: 1 1 100%;
                    }
                    .money,
                    .address {
                        flex: 0 1 50%;
                        font-size: .28rem;
                        line-height: .28rem;
                    }
                    .money {
                        .rmb,
                        .pay {
                            color: $color-orange;
                        }
                        .rmb {
                            font-size: .24rem;
                        }
                        .pay {
                            font-size: .4rem;
                        }
                    }
                    .address {
                        flex: 0 1 50%;
                        text-align: right;
                    }
                }
            }
        }
    }
</style>
