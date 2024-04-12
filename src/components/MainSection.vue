
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
    <div class="intro-tit-wrap">
        <div class="content-box">
            <img src="@/assets/image/logo_symbol2.png" alt="원투플레이">
            <h5>원투플레이</h5>
            <p>                    
                놀고 싶은 아이들을 위한 숲 속 별장<br>
                원투플레이와 함께 하세요.<br class="m-br">
            </p>
        </div>
    </div>
    <section id="room-preview-section">
        
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
            var mainPagination = document.querySelector('.swiper-pagination.swiper-pagination-fraction');
            document.querySelector('.swiper-pagination-current').style = "margin-right:10px;";
            document.querySelector('.swiper-pagination-total').style = "margin-left:10px;"
            for (var i = 0; i < mainPagination.childNodes.length; i++) {
                var node = mainPagination.childNodes[i];
                if (node.nodeName === "#text") {
                    // "#text" 노드의 내용을 변
                    node.nodeValue = "―――――――――";
                }
            }
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