<template>
    <header class="top-header">
        <div class="header-back">
            <span class="icon iconfont"></span>
        </div>
        <div class="header-search">
            <!-- <input type="text"> -->
            输入
        </div>
        <div class="header-city">
            <span class="icon iconfont">城市</span>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>
    .top-header {
        display: flex;
        height: .86rem;
        line-height: .86rem;
        background: $header-bg-color;
        color: $base-color;
        .icon {
            display: block;
            text-align: center;
        }
        .header-back {
            float: left;
            width: .64rem;
            .icon {
                &:before {
                    content: "\e622";
                }
            }
        }
        .header-search {
            flex: 1;
            border-radius: .1rem;
            height: .64rem;
            margin-top: .12rem;
            margin-left: .2rem;
            background-color: $base-color;
            color: $base-color-gray;
        }
        .header-city {
            float: right;
            width: 1.24rem;
            text-align: center;
            .icon {
                &:after {
                    content: "\e6aa";
                }
            }
        }
    }
</style>
