<template>
    <div>
        <HeaderLayOut fonts="nexon container" />
        <SliderSection />
        <ImageSection attr="section nexon" layout="container" />
        <ImageTextSection attr="section nexon" layout="container" />
        <CardSection attr="section nexon" layout="container" />
        <BannerSection attr="gmaket" />
        <TextSection attr="section nexon" layout="container" />
        <FooterLayOut attr="section nexon" layout="container" />
    </div>
</template>

<script>
import HeaderLayOut from './components/layOut/HeaderLayOut.vue';
import SliderSection from './components/section/SliderSection.vue';
import ImageSection from './components/section/imageSection.vue';
import ImageTextSection from './components/section/imageTextSection.vue';
import CardSection from './components/section/cardSection.vue';
import BannerSection from './components/section/bannerSection.vue';
import TextSection from './components/section/textSection.vue';
import FooterLayOut from './components/layOut/FooterLayOut.vue';

export default {
    name: 'App',
    components: {
        HeaderLayOut,
        SliderSection,
        ImageSection,
        ImageTextSection,
        CardSection,
        BannerSection,
        TextSection,
        FooterLayOut,
    },
};
</script>
