<template>
    <div id = "yousheng">
        <div class="swiper-container" ref = "swiperContainer">
            <div class="swiper-wrapper">
                <div class="swiper-slide"><img src = "../../../public/img/book-icon1.jpg"></img></div>
                <div class="swiper-slide"><img src = "../../../public/img/book-icon2.jpg"></img></div>
                <div class="swiper-slide"><img src = "../../../public/img/book-icon3.jpg"></img></div>
            </div>
        </div>
        <div class = "yousheng-bottom">
            <Classify/>
            <Albums/>
        </div>
    </div>
</template>
<script>
     import Classify from "components/classify";
    import Albums from "components/albumList"
    import Swiper from "swiper";
    import "swiper/dist/css/swiper.css";
    export default{
        name:"YouSheng",
        //必须要是再能获取到真实的DOM节点，才能用轮播
        components:{
            Classify,
            Albums
        },
        mounted(){
            var mySwiper = new Swiper(this.$refs.swiperContainer, {
                speed: 500,
                spaceBetween: 10,
                loop: true, // 循环模式选项
                autoplay: {
                    disableOnInteraction: false
                },
                slidesPerView: "auto",
                centeredSlides:true,
            });
        }
    }
</script>
<style>

#yousheng{
    font-size: .12rem;
    padding-top: .2rem;
}
.swiper-container{
    width: 3.75rem;
    height: 1.26rem;
}
.swiper-wrapper{
    width: 3.75rem;
    height: 1.26rem;
    text-align: center;
    line-height: 1.26rem;
}
.swiper-wrapper .swiper-slide{
    width:80%;
    height: 100%;
    line-height: 1.26rem;
}
.swiper-wrapper .swiper-slide img{
    width:100%;
    height: 100%;
    border-radius: .2rem;
}

.yousheng-bottom{
    width: 100%
}
</style>