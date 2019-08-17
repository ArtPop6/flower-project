<template>
    <div class="aw">
        <swiper :options="swiperOption">
            <swiper-slide>
                <img src="../assets/tasha.png" style="width: 100%" />
            </swiper-slide>
            <swiper-slide>
                <img src="../assets/haidi.png" style="width: 100%" />
            </swiper-slide>
            <swiper-slide>
                <img src="../assets/timg.png" style="width: 100%" />
            </swiper-slide>
            <swiper-slide>4</swiper-slide>
            <swiper-slide>5</swiper-slide>
        </swiper>
        <div class="swiper-pagination" slot="pagination"></div>
    </div>
</template>
<script>
export default {
    name: 'Awesome',
    data() {
        return {
            swiperOption: {
                spaceBetween: 30,
                centeredSlide: true,
                autoplay: {
                    delay: 2500,
                    disableOnInteraction: false
                },
                pagination: {
                    el: '.swiper-pagination',
                    clickable: true
                },
                loop: true
            }
        }
    },

}
</script>