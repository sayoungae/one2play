
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
        <div class="info-con">
            <div class="inner-con">
                <div class="img-box"><img src="" alt=""/></div>
                <div class="txt-box">
                    <div>
                        <span>SPACE</span>
                        <h3>Living & Kitchen</h3>
                        <p>거실 & 주방,</p>
                    </div>
                    <div>
                        <p>
                            거실은 펜션에서 휴식과 모임을 위한 아늑한 공간을 제공합니다.<br/>
                            이 곳에서 편안하게 쉬고, 함께 시간을<br/>
                            보내며 즐거운 추억을 만들어 보세요.<br/>
                            주방은 고객님들에게 편리한 요리 공간을 제공합니다.<br/>
                            가족과 친구들과 함께 식사를 준비하고 즐거운<br/>
                            식사와 추억을 남겨보세요.
                        </p>
                        <a href="#none">
                            Living & Kitchen
                            <div class="line-wrap">
                                <span class="line"></span>
                                <span class="line"></span>
                            </div>
                        </a>
                    </div>
                </div>
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