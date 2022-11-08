<template>
	<section id="cardType" class="parallax card__wrap" :class="attr">
		<h2>밤하늘 과 관련된 시</h2>
		<p>밤하늘 또는 야천(夜天)은 밤에 보이는 하늘을 이르는 말입니다.</p>
		<div class="card__inner" :class="layout">
			<article class="card">
				<figure class="card__header">
					<img src="../../assets/img/card_bg01.jpg" alt="고양이 사진1" />
				</figure>
				<div class="card__body">
					<h3 class="tit">저녁 에</h3>
					<p class="desc">
						저렇게 많은 별 중에서<br />
						별 하나가 나를 내려다본다<br />
						이렇게 많은 사람 중에서<br />
						그 별 하나를 쳐다본다
					</p>
					<a class="btn" href="/">
						더 자세히 보기
						<span aria-hidden="true">
							<svg width="81" height="8" viewBox="0 0 81 8" fill="none" xmlns="http://www.w3.org/2000/svg">
								<path
									d="M80.3536 4.35355C80.5488 4.15829 80.5488 3.84171 80.3536 3.64645L77.1716 0.464466C76.9763 0.269204 76.6597 0.269204 76.4645 0.464466C76.2692 0.659728 76.2692 0.976311 76.4645 1.17157L79.2929 4L76.4645 6.82843C76.2692 7.02369 76.2692 7.34027 76.4645 7.53553C76.6597 7.7308 76.9763 7.7308 77.1716 7.53553L80.3536 4.35355ZM0 4.5H80V3.5H0V4.5Z"
									fill="#B5B5B5"
								/>
							</svg>
						</span>
					</a>
				</div>
			</article>
			<article class="card">
				<figure class="card__header">
					<img src="../../assets/img/card_bg02.jpg" alt="고양이 사진2" />
				</figure>
				<div class="card__body">
					<h3 class="tit">어떤 마을</h3>
					<p class="desc">
						사람들이 착하게 사는지 별들이 많이 떴다<br />
						개울물 맑게 흐르는 곳에 마을을 이루고<br />
						물바가지에 떠담던 접동새소리 별 그림자<br />
						그 물로 쌀을 씻어 밥짓는 냄새 나면<br />
						굴뚝 가까이 내려오던<br />
						밥티처럼 따스한 별들이 뜬 마을을 지난다<br />
						사람들이 순하게 사는지 별들이 참 많이 떴다<br />
					</p>
					<a class="btn" href="/">
						더 자세히 보기
						<span aria-hidden="true">
							<svg width="81" height="8" viewBox="0 0 81 8" fill="none" xmlns="http://www.w3.org/2000/svg">
								<path
									d="M80.3536 4.35355C80.5488 4.15829 80.5488 3.84171 80.3536 3.64645L77.1716 0.464466C76.9763 0.269204 76.6597 0.269204 76.4645 0.464466C76.2692 0.659728 76.2692 0.976311 76.4645 1.17157L79.2929 4L76.4645 6.82843C76.2692 7.02369 76.2692 7.34027 76.4645 7.53553C76.6597 7.7308 76.9763 7.7308 77.1716 7.53553L80.3536 4.35355ZM0 4.5H80V3.5H0V4.5Z"
									fill="#B5B5B5"
								/>
							</svg>
						</span>
					</a>
				</div>
			</article>
			<article class="card">
				<figure class="card__header">
					<img src="../../assets/img/card_bg03.jpg" alt="고양이 사진3" />
				</figure>
				<div class="card__body">
					<h3 class="tit">별</h3>
					<p class="desc">
						어느날 거리엘 나갔다 비를 만나 지나치던 한 처마 아래 들어섰으려니 내 곁에도 역시 나와 한 가지로 멀구러미 하늘을 쳐다보고 비를 긋고 섰는 사나이가 있어, 그의 모습을 보아하니 문득 그 별이 생각났다. 밤마다 뜨락에 내려 우러러 보노라면 만천의 별들 가운데서도 가장 나의 별 가차이
						나도 모를, 항상 그늘 많은 별 하나-. 영원히 건널 수 없는 심연에 나누어져 말없이 서로 바라보고 지낼 수 밖에 없는 먼 먼 그 별, 그리고 나의 별!
					</p>
					<a class="btn" href="/">
						더 자세히 보기
						<span>
							<svg width="81" height="8" viewBox="0 0 81 8" fill="none" xmlns="http://www.w3.org/2000/svg">
								<path
									d="M80.3536 4.35355C80.5488 4.15829 80.5488 3.84171 80.3536 3.64645L77.1716 0.464466C76.9763 0.269204 76.6597 0.269204 76.4645 0.464466C76.2692 0.659728 76.2692 0.976311 76.4645 1.17157L79.2929 4L76.4645 6.82843C76.2692 7.02369 76.2692 7.34027 76.4645 7.53553C76.6597 7.7308 76.9763 7.7308 77.1716 7.53553L80.3536 4.35355ZM0 4.5H80V3.5H0V4.5Z"
									fill="B5B5B5"
								/>
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
