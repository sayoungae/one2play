
<template>
   <section id="main-visual-wrap">
        <div class="main-slide-wrap">
            <swiper class="slide-list" :options="mainSwiperOption">
                <swiper-slide>1</swiper-slide>
                <swiper-slide>2</swiper-slide>
                <swiper-slide>3</swiper-slide>
                <swiper-slide>4</swiper-slide>
                <swiper-slide>5</swiper-slide>
                <swiper-slide>6</swiper-slide>
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

export default {
	name: "main-slide",
	components:	{
       Swiper,
       SwiperSlide
	},
    data(){
        return{
            mainSwiperOption:{
                slidesPerView:1,
            }
        }
    }
}

</script>