<template>
    <div class="list" ref="wrapper">
        <div>
            <div class="area">
                <div class="title border-topbottom">当前城市</div>
                <div class="button-list">
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>

                </div>
            </div>

            <div class="area">
                <div class="title border-topbottom">热门城市</div>
                <div class="button-list">
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">上海</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">深圳</div>
                    </div>
                    <div class="button-wrapper">
                        <div class="button">西安</div>
                    </div>
                </div>
            </div>

            <div class="area">
                <div class="title border-topbottom">A</div>
                <div class="item-list">
                    <div class="item border-bottom">阿拉尔</div>
                    <div class="item border-bottom">阿拉善</div>
                    <div class="item border-bottom">阿克苏</div>
                    <div class="item border-bottom">阿拉伯</div>
                </div>
            </div>

            <div class="area">
                <div class="title border-topbottom">B</div>
                <div class="item-list">
                    <div class="item border-bottom">布鲁塞尔</div>
                    <div class="item border-bottom">布拉格</div>
                    <div class="item border-bottom">不列颠</div>
                    <div class="item border-bottom">卜县</div>
                </div>
            </div>

            <div class="area">
                <div class="title border-topbottom">C</div>
                <div class="item-list">
                    <div class="item border-bottom">重庆</div>
                    <div class="item border-bottom">成都</div>
                    <div class="item border-bottom">澄县</div>
                    <div class="item border-bottom">昌平</div>
                </div>
            </div>

            <div class="area">
                <div class="title border-topbottom">D</div>
                <div class="item-list">
                    <div class="item border-bottom">东城</div>
                    <div class="item border-bottom">多克阿斯顿</div>
                    <div class="item border-bottom">大名府</div>
                    <div class="item border-bottom">大连</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Bscroll from 'better-scroll'
    export default {
        name: "CityList",
        mounted () {
            this.scroll = new Bscroll(this.$refs.wrapper)
        }
    }
</script>

<style scoped lang="stylus">
    @import '~styles/varibles.styl'
    .border-topbottom
        &:before
            border-color: #ccc
        &:after
            border-color: #ccc
        .border-bottom
        &:before
            border-color: #ccc
    .list
        position: absolute
        overflow: hidden
        top: 1.58rem
        left: 0
        right: 0
        bottom: 0
        .title
            line-height: .54rem
            background: #eee
            padding-left: .2rem
            color: #666
            font-size: .26rem
        .button-list
            padding: .1rem .6rem .1rem .1rem
            overflow: hidden
            .button-wrapper
                float: left
                width: 33.33%
                .button
                    text-align: center
                    margin: .1rem
                    padding: .1rem 0
                    border-radius: .06rem
                    border: .02rem solid #ccc
        .item-list
            .item
                line-height: .76rem
                padding-left: .2rem
</style>
