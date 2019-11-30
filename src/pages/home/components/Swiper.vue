<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl">
            </swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name: "HomeSwiper",
    data () {
        return {
            swiperOption: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [
                {
                    id: '0001',
                    imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201910/e7eac5a5e99e6517c61b953c0fece63b.jpg_750x200_4b701cf8.jpg"
                },
                {
                    id: '0002',
                    imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/201911/14c86b17f55e4b639776b497178f8ef7.jpg_750x200_0d6b121a.jpg"
                },
                {
                    id: '0003',
                    imgUrl: "http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/b23a39921e8b78f38b61412d691d93ea.jpg_750x200_942ed7bd.jpg"
                }

            ]
        }
    }
}
</script>

<style scoped lang="stylus">
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fff
    .wrapper
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom 26.6%
        background #eee
        .swiper-img
            width: 100%
</style>
