
<template>
    <section id="main-visual-wrap">
        <div class="main-slide-wrap">
            <swiper class="slide-list"
            :spaceBetween="30"
            :effect="'fade'"
            :pagination="{clickable: true, type: 'fraction' }"
            :autoplay="{
                delay: 3000,
                disableOnInteraction: false,
            }"
            :modules="modules"
            
            @swiper="onSwiper"
            @slideChange="onSlideChange"
            >
                <swiper-slide v-for="mainSlide in 15" :key="mainSlide"></swiper-slide>
            </swiper>
            <div class="txt-box">
                <div class="title">healing forest</div>
                <p class="sub-txt">아이들의 미소와 웃음으로 가득한곳,<br/>자유롭게 뛰어놀수있는 특별한 공간</p>
            </div>
        </div>
    </section>
</template>
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation, Pagination, Autoplay, EffectFade } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import 'swiper/css/effect-fade';

export default {
	name: "main-slide",
	components:	{
        Swiper,
        SwiperSlide
	},
    setup() {
        const onSwiper = (swiper) => {
            console.log(swiper);
        };
        const onSlideChange = () => {
            console.log('slide change');
        };
        return {
            onSwiper,
            onSlideChange,
            modules: [Navigation, Pagination, Autoplay, EffectFade],
        };
    }
}

</script>