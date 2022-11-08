<template>
    <section id="imgType" class="parallax img__wrap" :class="attr">
        <h2>밤 풍경</h2>
        <p>밤의 별빛들을 보면 차분해 지는 느낌이 들어요.</p>
        <div class="image__inner" :class="layout">
            <article class="image" :class="text.imgClass" v-for="text in imageText" :key="text">
                <div class="image__box">
                    <h3 class="image__tit">{{ text.imgTit }}</h3>
                    <p class="image__desc">{{ text.imgDesc }}</p>
                    <a class="image__btn" :class="text.btnClass" :href="text.btnLink">자세히보기</a>
                </div>
            </article>
        </div>
    </section>
</template>
<script>
export default {
    props: {
        attr: String,
        layout: String,
    },
    data() {
        return {
            imageText: [
                {
                    imgTit: '밤 하늘',
                    imgDesc: '아름다운 밤 풍경을 보며 차분한 차 한잔을 하는것도 좋을것 같습니다. 혹은 명상을 하는게 어떠신가요?',
                    imgClass: 'img1',
                    btnClass: 'basic',
                    btnLink: '/',
                },
                {
                    imgTit: '오로라',
                    imgDesc:
                        '주로 지구의 북극권, 남극권 지역에서 관측할 수 있는 천문현상. 초고층 대기 중에 형형색색의 발광(發光)이 나타나며, 이 때문에번역할 경우 극광이라고도 부릅니다.',
                    imgClass: 'img2',
                    btnClass: 'brown',
                    btnLink: '/',
                },
            ],
        };
    },
};
</script>
<style>
/* imgType */
.image__inner {
    display: flex;
    justify-content: space-between;
}
.image {
    width: 49%;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    border-radius: 20px;
    padding: 210px 20px 20px 20px;
    box-sizing: border-box;
}
.img1 {
    background-image: url(../../assets/img/img_bg01_01.jpg);
    background-size: cover;
}
.img2 {
    background-image: url(../../assets/img/img_bg01_02.jpg);
    background-size: cover;
}
.image__box {
    margin: 30px;
}
.image__tit {
    font-size: 32px;
    color: #dadada;
    margin-bottom: 10px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
.image__desc {
    font-size: 16px;
    margin-bottom: 10px;
    line-height: 1.5;
    color: #b5b5b5;
    background-color: rgba(0, 0, 0, 0.08);
    backdrop-filter: blur(2px);
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
}
.image__btn {
    display: inline-block;
    font-size: 16px;
    padding: 10px 32px 8px 32px;
    background-color: #646aff;
    color: #030a1a;
    border-radius: 15px;
}
.image__btn.brown {
    background-color: #7c5df5;
}
@media (max-width: 960px) {
}
@media (max-width: 600px) {
    .image__inner {
        flex-direction: column;
    }
    .image {
        width: 100%;
        padding: 210px 20px 20px 20px;
    }
    .image:first-child {
        margin-bottom: 20px;
    }
    .image__tit {
        font-size: 24px;
    }
    .image__desc {
        font-size: 16px;
    }
}
</style>
