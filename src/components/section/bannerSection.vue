<template>
    <section id="bannerType" class="parallax banner__wrap" :class="attr">
        <h2 class="blind">{{ bannerText.title }}</h2>
        <div class="banner__inner">
            <h3 class="title">{{ bannerText.title }}</h3>
            <p class="desc">
                {{ bannerText.desc }}
                <a :href="bannerText.link" title="새로운페이지열림" target="_blank">{{ bannerText.link }}</a>
            </p>
            <span class="small">{{ smallDesc }}</span>
        </div>
    </section>
</template>
<script>
export default {
    props: {
        attr: String,
    },
    data() {
        return {
            bannerText: {
                title: '은하수',
                desc: '지구(태양계)에서 관측하는 우리 은하의 단면의 모습이다',
                link: 'syumay.tistory.com',
                smallDesc: '밤 하늘의 별',
            },
        };
    },
};
</script>
<style>
.banner__inner {
    background-image: url(../../assets/img/banner_bg01.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    text-align: center;
    padding: 120px 0;
    color: #dadada;
    padding: 100px;
}
.banner__inner .title {
    font-size: 50px;
    line-height: 1;
    font-weight: 300;
    margin-bottom: 40px;
}
.banner__inner .desc {
    display: inline-block;
    font-size: 24px;
    line-height: 1.5;
    font-weight: 300;
    margin-bottom: 70px;
    color: #b5b5b5;
    box-shadow: 5px 10px 30px #030a1a;
}
.banner__inner .small {
    display: block;
    font-size: 16px;
    text-decoration: underline;
    color: #b5b5b5;
}

.banner__inner .desc a {
    display: block;
    color: #b5b5b5;
}
.banner__inner .desc a:hover {
    color: #dadada;
}
@media (max-width: 960px) {
    .banner__inner {
        padding: 100px 0;
    }
}
@media (max-width: 600px) {
    .banner__inner {
        padding: 80px 0;
    }
    .banner__inner .title {
        font-size: 30px;
        margin-bottom: 20px;
    }
    .banner__inner .desc {
        font-size: 16px;
        margin-bottom: 40px;
    }
}
</style>
