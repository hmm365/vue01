<template>
    <section id="imgTextType" class="parallax imgText__wrap" :class="attr">
        <h2 class="blind">{{ imgTextTitle.title }}</h2>
        <div class="imgText__inner" :class="layout">
            <div class="imgText__txt">
                <span>{{ imgTextTitle.titlesmall }}</span>
                <h3>{{ imgTextTitle.title }}</h3>
                <p>{{ imgTextTitle.desc }}</p>
                <ul>
                    <li v-for="textLink in imgTextLink" :key="textLink">
                        <a :href="textLink.links">{{ textLink.linkName }}</a>
                    </li>
                </ul>
            </div>
            <div class="imgText__img" :class="textSite.siteImg" v-for="textSite in imgTextSite" :key="textSite">
                <a :class="textSite.btnColor" :href="textSite.alink">{{ textSite.sites }}</a>
            </div>
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
            imgTextTitle: {
                title: '밝디 밝고 밝은 보름달',
                desc: '달이 태양빛을 완전히 받아 앞면의 모든 모습이 드러나게 되는 현상입니다.',
                titlesmall: '나만 보고싶은',
            },
            imgTextLink: [
                {
                    linkName: '초승달',
                    links: '/',
                },
                {
                    linkName: '반달',
                    links: '/',
                },
                {
                    linkName: '상현망',
                    links: '/',
                },
                {
                    linkName: '보름달',
                    links: '/',
                },
                {
                    linkName: '하현망',
                    links: '/',
                },
                {
                    linkName: '초승달',
                    links: '/',
                },
                {
                    linkName: '그믐달',
                    links: '/',
                },
            ],
            imgTextSite: [
                { siteImg: 'img1', sites: '보름달 사이트', alink: '/', btnColor: '' },
                { siteImg: 'img1', sites: '초승달 사이트', alink: '/', btnColor: 'blue' },
            ],
        };
    },
};
</script>
<style>
/* imgTextType */
.imgText__inner {
    display: flex;
    justify-content: space-between;
}

.imgText__inner > div {
    width: 32%;
    height: 500px;
}
.imgText__txt {
}
.imgText__txt span {
    display: block;
    font-size: 16px;
    color: #666;
    text-decoration: underline;
    text-underline-position: under;
    margin-bottom: 20px;
}
.imgText__txt h3 {
    font-size: 50px;
    font-weight: 300;
    word-break: keep-all;
    margin-bottom: 20px;
    color: #dadada;
}
.imgText__txt p {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.5;
    color: #b5b5b5;
    margin-bottom: 10px;
}
.imgText__txt ul {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.6;
}
.imgText__txt ul li {
    position: relative;
    padding-left: 20px;
}
.imgText__txt ul li a {
    color: #b5b5b5;
}
.imgText__txt ul li::before {
    content: '';
    width: 5px;
    height: 5px;
    border-radius: 50%;
    position: absolute;
    left: 5px;
    top: 9px;
    background: #b5b5b5;
}
.imgText__img {
    border-radius: 100px 2px 5px 5px;
    position: relative;
}
.imgText__img a {
    background-color: #7c2b39;
    color: #dadada;
    font-size: 18px;
    padding: 10px 30px;
    border-radius: 30px;
    position: absolute;
    left: 30px;
    bottom: 30px;
    display: inline-block;
}
.imgText__img a.blue {
    background-color: #2b387c;
}
.imgText__img.img1 {
    background: url(../../assets/img/imgText_bg01.jpg) no-repeat center;
    background-size: cover;
}
.imgText__img.img2 {
    background: url(../../assets/img/imgText_bg02.jpg) no-repeat center;
    background-size: cover;
}

@media (max-width: 960px) {
    .imgText__inner {
        flex-wrap: wrap;
    }
    .imgText__inner > div.imgText__txt {
        width: 100%;
        height: auto;
        text-align: center;
    }
    .imgText__txt h3 {
        font-size: 40px;
    }
    .imgText__inner > div.imgText__img {
        width: 49%;
    }
    .imgText__txt ul {
        display: none;
    }
    .imgText__txt p {
        font-size: 16px;
        margin-bottom: 20px;
    }
}
@media (max-width: 600px) {
    .imgText__txt span {
        font-size: 14px;
        margin-bottom: 10px;
    }
    .imgText__txt h3 {
        font-size: 30px;
    }
    .imgText__txt p {
        font-size: 16px;
        margin-bottom: 50px;
    }
    .imgText__inner > div.imgText__img {
        width: 100%;
        height: 250px;
    }
    .imgText__img.img1 {
        margin-bottom: 20px;
    }

    .imgText__img a {
        left: 20px;
        bottom: 20px;
    }
}
</style>
