<template>
    <section id="cardType" class="parallax card__wrap" :class="attr">
        <h2>{{ cardTitle.title }}</h2>
        <p>{{ cardTitle.desc }}</p>
        <div class="card__inner" :class="layout">
            <article v-for="cardTexts in cardText" :key="cardTexts" class="card">
                <figure class="card__header">
                    <img :src="cardTexts.imgSrc" :alt="cardTexts.imgName" />
                </figure>
                <div class="card__body">
                    <h3 class="tit">{{ cardTexts.cardTitle }}</h3>
                    <p class="desc">
                        {{ cardTexts.cardDesc }}
                    </p>
                    <a class="btn" :href="cardTexts.btnLink">
                        더 자세히 보기
                        <span aria-hidden="true">
                            <svg width="81" height="8" viewBox="0 0 81 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path :d="cardTexts.cardIcon" :fill="cardTexts.cardIconFill" />
                            </svg>
                        </span>
                    </a>
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
            cardTitle: { title: '밤하늘 과 관련된 시', desc: '밤하늘 또는 야천(夜天)은 밤에 보이는 하늘을 이르는 말입니다.' },
            cardText: [
                {
                    imgSrc: 'assets/img/card_bg01.jpg',
                    imgName: '사진1',
                    cardTitle: '저녁 에',
                    cardDesc: '저렇게 많은 별 중에서 \n별 하나가 나를 내려다본다\n이렇게 많은 사람 중에서\n그 별 하나를 쳐다본다',
                    btnLink: '/',
                    cardIcon:
                        'M80.3536 4.35355C80.5488 4.15829 80.5488 3.84171 80.3536 3.64645L77.1716 0.464466C76.9763 0.269204 76.6597 0.269204 76.4645 0.464466C76.2692 0.659728 76.2692 0.976311 76.4645 1.17157L79.2929 4L76.4645 6.82843C76.2692 7.02369 76.2692 7.34027 76.4645 7.53553C76.6597 7.7308 76.9763 7.7308 77.1716 7.53553L80.3536 4.35355ZM0 4.5H80V3.5H0V4.5Z',
                    cardIconFill: '#B5B5B5',
                },
                {
                    imgSrc: 'assets/img/card_bg02.jpg',
                    imgName: '사진2',
                    cardTitle: '어떤 마을',
                    cardDesc:
                        '​​저렇게 많은 중에서\n별 하나가 나를 내려다본다.\n이렇게 많은 사람 중에서\n그 별 하나를 쳐다본다.\n​​밤이 깊을수록 별은\n밝음 속에 사라지고\n나는 어둠 속에 사라진다.\n​​이렇게 정다운\n너 하나 나 하나는\n어디서 무엇이 되어 다시 만나랴.',
                    btnLink: '/',
                    cardIcon:
                        'M80.3536 4.35355C80.5488 4.15829 80.5488 3.84171 80.3536 3.64645L77.1716 0.464466C76.9763 0.269204 76.6597 0.269204 76.4645 0.464466C76.2692 0.659728 76.2692 0.976311 76.4645 1.17157L79.2929 4L76.4645 6.82843C76.2692 7.02369 76.2692 7.34027 76.4645 7.53553C76.6597 7.7308 76.9763 7.7308 77.1716 7.53553L80.3536 4.35355ZM0 4.5H80V3.5H0V4.5Z',
                    cardIconFill: '#B5B5B5',
                },
                {
                    imgSrc: 'assets/img/card_bg03.jpg',
                    imgName: '사진3',
                    cardTitle: '별',
                    cardDesc:
                        '어느날 거리엘 나갔다 비를 만나 지나치던 한 처마 아래 들어섰으려니 내 곁에도 역시 나와 한 가지로 멀구러미 하늘을 쳐다보고비를 긋고 섰는 사나이가 있어, 그의 모습을 보아하니 문득 그 별이 생각났다. 밤마다 뜨락에 내려 우러러 보노라면 만천의 별들가운데서도 가장 나의 별 가차이 나도 모를, 항상 그늘 많은 별 하나-. 영원히 건널 수 없는 심연에 나누어져 말없이 서로바라보고 지낼 수 밖에 없는 먼 먼 그 별, 그리고 나의 별!',
                    btnLink: '/',
                    cardIcon:
                        'M80.3536 4.35355C80.5488 4.15829 80.5488 3.84171 80.3536 3.64645L77.1716 0.464466C76.9763 0.269204 76.6597 0.269204 76.4645 0.464466C76.2692 0.659728 76.2692 0.976311 76.4645 1.17157L79.2929 4L76.4645 6.82843C76.2692 7.02369 76.2692 7.34027 76.4645 7.53553C76.6597 7.7308 76.9763 7.7308 77.1716 7.53553L80.3536 4.35355ZM0 4.5H80V3.5H0V4.5Z',
                    cardIconFill: '#B5B5B5',
                },
            ],
        };
    },
};
</script>
<style>
/* cardType */
.card__inner {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}
.card {
    width: 32%;
    background-color: rgba(71, 47, 193, 0.3);
    border-radius: 23px 23px 20px 20px;
}

.card__header img {
    border-radius: 20px 20px 0 0;
}
.card__body {
    padding: 24px;
}
.card__body .tit {
    font-size: 24px;
    margin-bottom: 10px;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
    color: #dadada;
}
.card__body .desc {
    font-size: 18px;
    line-height: 1.4;
    color: #b5b5b5;
    margin-bottom: 20px;
    font-weight: 300;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
}
.card__body .btn {
    color: #b5b5b5;
    font-size: 16px;
    margin-bottom: 24px;
}
@media (max-width: 960px) {
    .card {
        width: 49%;
    }
    .card:last-child {
        display: none;
    }
}
@media (max-width: 600px) {
    .card {
        width: 100%;
    }
    .card:first-child {
        margin-bottom: 20px;
    }
    .card__body {
        padding: 20px;
    }
    .card__body .tit {
        font-size: 18px;
    }
    .card__body .desc {
        font-size: 16px;
    }
}
</style>
