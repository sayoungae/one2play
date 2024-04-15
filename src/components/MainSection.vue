
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
                <div class="img-box"><img src="@/assets/image/room_preview_img1.jpg" alt=""/></div>
                <div class="txt-box">
                    <div class="tit">
                        <span>SPACE</span>
                        <h3>Living & Kitchen</h3>
                        <p>거실 & 주방,</p>
                    </div>
                    <div class="txt">
                        <p>
                            거실은 펜션에서 휴식과 모임을 위한 아늑한 공간을 제공합니다.<br/>
                            이 곳에서 편안하게 쉬고, 함께 시간을<br/>
                            보내며 즐거운 추억을 만들어 보세요.<br/>
                            주방은 고객님들에게 편리한 요리 공간을 제공합니다.<br/>
                            가족과 친구들과 함께 식사를 준비하고 즐거운<br/>
                            식사와 추억을 남겨보세요.
                        </p>
                        <a href="#none" class="link">
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
        <div class="info-con">
            <div class="inner-con">
                <div class="txt-box">
                    <div class="tit">
                        <span>SPACE</span>
                        <h3>Jungle Room</h3>
                        <p>정글룸,</p>
                    </div>
                    <div class="txt">
                        <p>
                            소나무 원목으로 제작된 이층 놀이터와<br/>
                            오두막,그린 플랜테리어 월, 각종 동물친구들<br/>
                            동물러버 친구들 모두 모이세요<br/>
                            Welcome to the One two Jungle !!!
                        </p>
                        <a href="#none" class="link">
                            Jungle Room
                            <div class="line-wrap">
                                <span class="line"></span>
                                <span class="line"></span>
                            </div>
                        </a>
                    </div>
                </div>
                <div class="img-box"><img src="@/assets/image/room_preview_img2.jpg" alt=""/></div>
            </div>
        </div>
        <div class="info-con">
            <div class="inner-con">
                <div class="img-box"><img src="@/assets/image/room_preview_img3.jpg" alt=""/></div>
                <div class="txt-box">
                    <div class="tit">
                        <span>SPACE</span>
                        <h3>Bedroom 2F</h3>
                        <p>침실2층,</p>
                    </div>
                    <div class="txt">
                        <p>
                            2층의 침실은 아름다운 전망과 조용한 분위기를 제공합니다.<br/>
                            이곳에서 자연의 아름다움을 감상하며 휴식을 취하고,<br/>
                            편안한 밤을 보내보세요.
                        </p>
                        <a href="#none" class="link">
                            Bedroom 2F
                            <div class="line-wrap">
                                <span class="line"></span>
                                <span class="line"></span>
                            </div>
                        </a>
                    </div>
                </div>
            </div>
        </div>
        <div class="info-con">
            <div class="inner-con">
                <div class="txt-box">
                    <div class="tit">
                        <span>SPACE</span>
                        <h3>Bedroom 1F</h3>
                        <p>정글룸,</p>
                    </div>
                    <div class="txt">
                        <p>
                            소나무 원목으로 제작된 이층 놀이터와<br/>
                            오두막,그린 플랜테리어 월, 각종 동물친구들<br/>
                            동물러버 친구들 모두 모이세요<br/>
                            Welcome to the One two Jungle !!!
                        </p>
                        <a href="#none" class="link">
                            Jungle Room
                            <div class="line-wrap">
                                <span class="line"></span>
                                <span class="line"></span>
                            </div>
                        </a>
                    </div>
                </div>
                <div class="img-box"><img src="@/assets/image/room_preview_img4.jpg" alt=""/></div>
            </div>
        </div>
    </section>
    <section id="sub-visual-section">
        <div class="bg">
            <div class="inner-con">
                <div class="tit-wrap">
                    <h3>Want to Play</h3>
                    <p>
                        <span>
                            아빠와 엄마가 직접 만든 집
                        </span>
                        <span>
                            원투플레이로 초대합니다.
                        </span>
                    </p>
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
        const onSwiper = () => {
            //console.log(swiper);
            var mainPagination = document.querySelector('.swiper-pagination.swiper-pagination-fraction');
            document.querySelector('.swiper-pagination-current').style = "margin-right:10px;";
            document.querySelector('.swiper-pagination-total').style = "margin-left:10px;"
            for (var i = 0; i < mainPagination.childNodes.length; i++) {
                var node = mainPagination.childNodes[i];
                if (node.nodeName === "#text") {
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