<template>
  <v-app>
    <home-carousel></home-carousel>
    <home-about></home-about>
    <home-about-2></home-about-2>
    <home-research></home-research>
    <home-news></home-news>
    <home-parallax></home-parallax>
    <home-martensite></home-martensite>
    <home-member></home-member>
    <home-contact></home-contact>
  </v-app>
</template>

<script>
import HomeCarousel from '../components/HomeView/HomeCarousel.vue';
import HomeAbout from '../components/HomeView/HomeAbout.vue';
import HomeAbout2 from '../components/HomeView/HomeAbout2.vue';
import HomeResearch from '../components/HomeView/HomeResearch.vue';
import HomeNews from '../components/HomeView/HomeNews.vue';
import HomeParallax from '../components/HomeView/HomeParallax.vue';
import HomeMember from '../components/HomeView/HomeMember.vue';
import HomeMartensite from '../components/HomeView/HomeMartensite.vue';
import HomeContact from '../components/HomeView/HomeContact.vue';

export default {
  components: {
    HomeCarousel,
    HomeAbout,
    HomeAbout2,
    HomeResearch,
    HomeNews,
    HomeParallax,
    HomeMember,
    HomeMartensite,
    HomeContact
  },
  data () {
    return {}
  },
}

</script>