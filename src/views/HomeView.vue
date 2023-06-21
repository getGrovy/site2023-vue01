<template>
  <main>
    <SliderSection attr="header__wrap , gmarket5, section " />
    <IntroSection attr="intro__wrap section gmarket5 bg-blue" />
    <PortSection attr="port__wrap section gmarket5 center bg-blue" />
    <YoutubeSection attr="youtube__wrap gmarket5 section" />
    <UnsplashSection attr="unsplash__wrap gmarket5 section bg-blue" />
    <MovieSection attr="movie__wrap gmarket5 section" />
  </main>
</template>

<script>
import SliderSection from "@/components/section/SliderSection.vue";
import IntroSection from "@/components/section/IntroSection.vue";
import PortSection from "@/components/section/PortSection.vue";
import MovieSection from "@/components/section/MovieSection.vue";
import YoutubeSection from "@/components/section/YoutubeSection.vue";
import UnsplashSection from "@/components/section/UnsplashSection.vue";

export default {
  components: {
    IntroSection,
    SliderSection,
    PortSection,
    MovieSection,
    YoutubeSection,
    UnsplashSection,
  },
};
</script>
