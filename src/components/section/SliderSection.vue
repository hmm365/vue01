<template>
    <section id="sliderType" class="slider__wrap">
        <h2 class="blind">슬라이드영역</h2>
        <div class="slider__inner">
            <swiper
                :spaceBetween="30"
                :centeredSlides="true"
                :autoplay="{
                    delay: 2500,
                    disableOnInteraction: false,
                }"
                :navigation="true"
                :pagination="true"
                :modules="modules"
                class="mySwiper"
            >
                <swiper-slide v-for="sliderDesc in sliderDesc" :key="sliderDesc"
                    ><div class="desc">
                        <span>{{ sliderDesc.smallTit }}</span>
                        <h3>{{ sliderDesc.title }}</h3>
                        <p>{{ sliderDesc.desc }}</p>
                        <div class="btn">
                            <a :href="sliderDesc.btnlink">자세히 보기</a>
                            <a :href="sliderDesc.btnSiteLink" class="black">사이트 보기</a>
                        </div>
                    </div>
                </swiper-slide>
            </swiper>
        </div>
    </section>
</template>
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
import { Navigation, Pagination, Autoplay } from 'swiper';

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
            modules: [Navigation, Pagination, Autoplay],
        };
    },
    data() {
        return {
            sliderDesc: [
                {
                    smallTit: 'night skys',
                    title: '별빛 하늘',
                    desc: '밤의 별빛들을 보면 차분해 지는 느낌이 들어요.\n여러분의 밤하늘을 찍어주세요.',
                    btnlink: '/',
                    btnSiteLink: '/',
                },
                {
                    smallTit: 'night skys',
                    title: '별빛 하늘',
                    desc: '밤의 별빛들을 보면 차분해 지는 느낌이 들어요.\n여러분의 밤하늘을 찍어주세요.',
                    btnlink: '/',
                    btnSiteLink: '/',
                },
                {
                    smallTit: 'night skys',
                    title: '별빛 하늘',
                    desc: '밤의 별빛들을 보면 차분해 지는 느낌이 들어요.\n여러분의 밤하늘을 찍어주세요.',
                    btnlink: '/',
                    btnSiteLink: '/',
                },
            ],
        };
    },
};
</script>

<style>
.slider__inner {
    margin-top: 70px;
}
.slider {
    position: relative;
}
.slider__img {
    background: url(../../assets/img/slider_bg01.jpg) no-repeat center / cover;
}
.slider__img .desc {
    max-width: 1160px;
    margin: 0 auto;
    padding: 100px 20px;
}
.slider__img .desc span {
    font-size: 16px;
    background-color: #030a1a;
    padding: 1px 14px 0 14px;
    border-radius: 30px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
    color: #b5b5b5;
}
.slider__img .desc h3 {
    font-size: 110px;
    font-weight: 300;
    line-height: 1;
    color: #dadada;
    text-transform: uppercase;
    margin-bottom: 16px;
    margin-left: -8px;
}
.slider__img .desc p {
    font-size: 20px;
    font-weight: 300;
    color: #b5b5b5;
    line-height: 1.35;
    margin-bottom: 130px;
}
.slider__img .desc .btn a {
    font-size: 16px;
    background-color: #dadada;
    padding: 11px 50px;
    display: inline-block;
}
.slider__img .desc .btn a.black {
    background: #030a1a;
    color: #b5b5b5;
}
.slider__arrow a {
    position: absolute;
    top: 50%;
    width: 30px;
    height: 56px;
    transform: translateY(-50%);
    background-image: url(../../assets/img/slider_icon.svg);
}
.slider__arrow a.left {
    left: 20px;
}
.slider__arrow a.right {
    right: 20px;
    background-position: -40px 0;
}
.slider__dot {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 25px;
}
.slider__dot a {
    display: inline-block;
    width: 16px;
    height: 16px;
    background-image: url(../../assets/img/slider_icon.svg);
    background-position: -20px -70px;
}

.slider__dot a.active {
    background-position: 0 -70px;
}
.slider__dot a.play {
    background-position: -40px -70px;
}
.slider__dot a.stop {
    background-position: -60px -70px;
}

.swiper-slide {
    position: relative;
}
.swiper-slide {
    background: url(../../assets/img/slider_bg01.jpg) no-repeat center / cover;
}
.swiper-slide:nth-child(2) {
    background: url(../../assets/img/slider_bg02.jpg) no-repeat center / cover;
}
.swiper-slide:nth-child(3) {
    background: url(../../assets/img/slider_bg03.jpg) no-repeat center / cover;
}
.swiper-slide .desc {
    max-width: 1160px;
    margin: 0 auto;
    padding: 100px 20px;
    box-sizing: border-box;
}
.swiper-slide .desc span {
    font-size: 16px;
    background-color: #030a1a;
    padding: 1px 14px 0 14px;
    border-radius: 30px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
    color: #b5b5b5;
}
.swiper-slide .desc h3 {
    font-size: 110px;
    font-weight: 300;
    line-height: 1;
    color: #dadada;
    text-transform: uppercase;
    margin-bottom: 16px;
    margin-left: -8px;
}
.swiper-slide .desc p {
    font-size: 20px;
    font-weight: 300;
    color: #b5b5b5;
    line-height: 1.35;
    margin-bottom: 130px;
}
.swiper-slide .desc .btn a {
    font-size: 16px;
    background-color: #dadada;
    padding: 11px 50px;
    display: inline-block;
}
.swiper-slide .desc .btn a.black {
    background: #030a1a;
    color: #b5b5b5;
}

.swiper-button-next,
.swiper-button-prev {
    width: 30px !important;
    height: 56px !important;
    transform: translateY(-30%);
    background-image: url(../../assets/img/slider_icon.svg);
}
.swiper-button-next {
    background-position: -40px 0;
}
.swiper-pagination-bullet {
    width: 16px !important;
    height: 16px !important;
    background-image: url(../../assets/img/slider_icon.svg) !important;
    background-position: -20px -70px !important;
    background-color: transparent !important;
    opacity: 1 !important;
}
.swiper-pagination-bullet-active {
    background-position: 0px -70px !important;
}
.swiper-button-prev:after,
.swiper-rtl .swiper-button-next:after,
.swiper-button-next:after,
.swiper-rtl .swiper-button-prev:after {
    content: '';
}
.swiper-button {
    position: absolute;
    left: 50%;
    bottom: 14px;
    z-index: 1000;
    margin-left: 40px;
    display: flex;
}
.swiper-button-stop {
    background-image: url(../../assets/img/slider_icon.svg);
    background-position: -60px -70px;
    width: 16px;
    height: 16px;
    cursor: pointer;
}
.swiper-button-play {
    background-image: url(../../assets/img/slider_icon.svg);
    background-position: -40px -70px;
    width: 16px;
    height: 16px;
    cursor: pointer;
}

@media (max-width: 960px) {
    .swiper-slide .desc {
        width: 100%;
        text-align: center;
    }
    .swiper-slide .desc h3 {
        font-size: 70px;
    }
}
@media (max-width: 600px) {
    .swiper-slide .desc {
        padding: 80px 0;
    }
    .swiper-slide .desc h3 {
        font-size: 40px;
    }
    .swiper-slide .desc p {
        font-size: 16px;
        margin-bottom: 50px;
    }
    .swiper-slide .desc .btn a {
        padding: 10px 25px;
    }
    .swiper-slide .desc span {
        font-size: 14px;
    }
}
</style>
