<template>
    <div>
        <div class="banner" @click="handleBannerClick">
            <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_600x330_f922b488.jpg">
            <div class="banner-info">
                <div class="banner-title">
                    故宫（AAAAA景区）
                </div>
                <div class="banner-number">
                    <span class="iconfont banner-icon">&#xe60f;</span>
                    12
                </div>
            </div>
        </div>
        <common-gallary
            :imgs="imgs"
            v-show="showGalary"
            @close="handleGallaryClose"
        ></common-gallary>
    </div>
</template>

<script>
    import CommonGallary from 'common/gallary/Gallary'
    export default {
        name: "DetailBanner",
        components: {
            CommonGallary
        },
        data () {
            return {
                imgs: [
                    'http://img1.qunarzz.com/sight/p0/1909/4e/4e1afc2e1133ade7a3.img.jpg_r_800x800_d3eb324d.jpg',
                    'http://img1.qunarzz.com/sight/p0/1907/ca/ca68bd95bc36bdba3.img.jpg_r_800x800_33169c4b.jpg'
                ],
                showGalary: false
            }
        },
        methods: {
            handleBannerClick () {
                this.showGalary = true;
            },
            handleGallaryClose () {
                this.showGalary = false;
            }
        }
    }
</script>

<style scoped lang="stylus">
    .banner
        position: relative
        overflow: hidden
        height: 0
        padding-bottom: 55%
        .banner-img
            width: 100%
        .banner-info
            display: flex
            position: absolute
            left: 0
            right: 0
            bottom: 0
            line-height: .6rem
            color: #fff
            background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,0.8))
            .banner-title
                font-size: .32rem
                padding: 0 .2rem
                flex: 1
            .banner-number
                height: .32rem
                line-height: .32rem
                margin-top: .14rem
                padding: 0 .4rem
                border-radius: .2rem
                background: rgba(0,0,0, .8)
                font-size: .24rem
                .banner-icon
                    font-size: .24rem
</style>
