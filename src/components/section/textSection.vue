<template>
	<section id="textType" class="parallax text__wrap" :class="attr">
		<span>한편의 시</span>
		<h2 class="mb70">밤하늘과 별과 밤에 관한 시</h2>
		<div class="text__inner" :class="layout">
			<div class="text t1">
				<h3 class="text__title">새벽 지친 별</h3>
				<p class="text__desc">
					밤이면 고총 아래 고개 숙이고<br />
					낮이면 하늘 보고 웃음 좀 웃고<br />
					너른들 쓸쓸하여 외론 할미꽃<br />
					아무도 몰래 지는 새벽 지친 별
				</p>
				<a href="#" class="text__btn">더보기</a>
			</div>
			<div class="text t2">
				<h3 class="text__title">유리창1</h3>
				<p class="text__desc">
					유리에 차고 슬픈 것이 어린거린다.<br />
					열없이 붙어 서서 입김을 흐리우니<br />
					길들은 양 언 날개를 파다거린다.
				</p>
				<a href="#" class="text__btn">더보기</a>
			</div>
			<div class="text t3">
				<h3 class="text__title">별</h3>
				<p class="text__desc">
					즐거운 날 밤에는 한 개도 없더니<br />
					한 개도 없더니 마음 슬픈 밤에는 하늘 가득 별이다.<br />
					수만 개일까 수십만 갤까 울고 싶은 밤에는 가슴에도 별이다. 온 세상이 별이다.
				</p>
				<a href="#" class="text__btn">더보기</a>
			</div>
			<div class="text t4">
				<h3 class="text__title">별 하나</h3>
				<p class="text__desc">
					별을 보았다.<br />
					깊은밤 혼자 바라보는 별 하나.<br />
					저 별은 하늘아이들이 사는집의 쬐그만 초인종. 문득 가득히 누르고 싶다.
				</p>
				<a href="#" class="text__btn">더보기</a>
			</div>
			<div class="text t5">
				<h3 class="text__title">서시</h3>
				<p class="text__desc">
					죽는 날까지 하늘을 우러러 한 점 부끄럼이 없기를,<br />
					잎새에 이는 바람에도 나는 괴로워했다.<br />
					별을 노래하는 마음으로 모든 죽어가는 것을 사랑해야지 그리고 나한테 주어진 길을 걸어가야겠다.<br />
					오늘 밤에도 별이 바람에 스치운다.
				</p>
				<a href="#" class="text__btn">더보기</a>
			</div>
			<div class="text t6">
				<h3 class="text__title">별 헤는 밤</h3>
				<p class="text__desc">
					별 하나에 추억과<br />
					별 하나에 사랑과<br />
					별 하나에 쓸쓸함과<br />
					별 하나에 동경과<br />
					별 하나에 시와<br />
					별 하나에 어머니, 어머니.
				</p>
				<a href="#" class="text__btn">더보기</a>
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
};
</script>
<style>
/* textType */
.text__inner {
	display: flex;
	flex-wrap: wrap;
	justify-content: space-between;
}
.text {
	width: 32%;
	margin-bottom: 2%;
	padding: 20px;
	box-sizing: border-box;
	border-radius: 10px;
	transition: background 0.6s;
	background: rgba(71, 47, 193, 0.3);
}
.text:hover {
	background: rgba(95, 71, 214, 0.6);
}

.text__title {
	font-size: 24px;
	line-height: 1;
	margin-bottom: 10px;
	white-space: nowrap;
	text-overflow: ellipsis;
	position: relative;
	padding-top: 75px;
	color: #b5b5b5;
}
.text__title::before {
	content: "";
	position: absolute;
	left: 0;
	top: 0;
	width: 60px;
	height: 60px;
	border-radius: 50%;
	background: url("../../assets/img/text_icon.svg");
}
.text.t1 .text__title::before {
	background-position: 0 0;
}
.text.t2 .text__title::before {
	background-position: -60px 0;
}
.text.t3 .text__title::before {
	background-position: -120px 0;
}
.text.t4 .text__title::before {
	background-position: -180px 0;
}
.text.t5 .text__title::before {
	background-position: -240px 0;
}
.text.t6 .text__title::before {
	background-position: -300px 0;
}
.text__desc {
	font-size: 18px;
	font-weight: 300;
	overflow: hidden;
	text-overflow: ellipsis;
	display: -webkit-box;
	-webkit-line-clamp: 3;
	-webkit-box-orient: vertical;
	color: #b5b5b5;
	margin-bottom: 20px;
}
.text__btn {
	font-size: 16px;
	line-height: 1;
	text-decoration: underline;
	text-underline-position: under;
	color: #b5b5b5;
}
@media (max-width: 960px) {
	.text {
		width: 49%;
		margin-bottom: 10px;
	}
}
@media (max-width: 600px) {
	.text__title {
		font-size: 20px;
	}
	.text__desc {
		font-size: 16px;
	}
	.text__title::before {
		width: 40px;
		height: 40px;
	}
	.text.t1 .text__title::before {
		background-position: -10px -10px;
	}
	.text.t2 .text__title::before {
		background-position: -70px -10px;
	}
	.text.t3 .text__title::before {
		background-position: -130px -10px;
	}
	.text.t4 .text__title::before {
		background-position: -190px -10px;
	}
	.text.t5 .text__title::before {
		background-position: -250px -10px;
	}
	.text.t6 .text__title::before {
		background-position: -310px -10px;
	}
}
@media (max-width: 480px) {
	.text {
		width: 100%;
	}
	.text:last-child {
		margin-bottom: 0;
	}
}
</style>
