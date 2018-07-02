<template>
    <header class="top-header">
        <div class="header-back">
            <span class="icon iconfont"></span>
        </div>
        <div class="header-search">
            <span class="icon iconfont"></span>
            <input type="text" :placeholder="placeholder">
        </div>
        <div class="header-city">
            <span class="icon iconfont">城市</span>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data () {
        return {
            placeholder: '请输入'
        }
    }
}
</script>

<style lang="scss">
    .top-header {
        display: flex;
        height: .86rem;
        line-height: .86rem;
        background: $header-bg-color;
        color: $color-white;
        .icon {
            display: block;
            text-align: center;
        }
        .header-back {
            //float: left;
            width: .86rem;
            .icon {
                &:before {
                    content: "\e622";
                }
            }
        }
        .header-search {
            flex: 1;
            height: .64rem;
            line-height: .64rem;
            margin-top: .12rem;
            background-color: $color-white;
            border-radius: .1rem;
            color: $color-gray;
            overflow: hidden;
            input {
                display: inline-block;
                width: 100%;
                height: 100%;
                border: none;
                padding: 3px 12px 3px .64rem;
                box-sizing: border-box;
            }
            .icon {
                display: inline-block;
                position: absolute;
                width: .64rem;
                &:before {
                    content: "\e60d";
                }
            }
        }
        .header-city {
            //float: right;
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
