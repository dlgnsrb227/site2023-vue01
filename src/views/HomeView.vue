<template>
  <main>
    <SliderSection attr="slider__wrap section" />
    <IntroSection attr="intro__wrap bg-blue section" />
    <!-- <ProfileSection /> -->
    <PortSection attr="port__wrap section center" />
    <YoutubeSection attr="youtube__wrap bg-blue section" />
    <UnsplashSection attr="unsplash__wrap section" />
    <MovieSection attr="movie__wrap section bg-blue" />
  </main>
</template>

<script>
// @ is an alias to /src
import SliderSection from "@/components/section/SliderSection.vue";
import IntroSection from "@/components/section/IntroSection.vue";
// import ProfileSection from "@/components/section/ProfileSection.vue";
import PortSection from "@/components/section/PortSection.vue";
import YoutubeSection from "@/components/section/YoutubeSection.vue";
import UnsplashSection from "@/components/section/UnsplashSection.vue";
import MovieSection from "@/components/section/MovieSection.vue";

export default {
  components: {
    SliderSection,
    IntroSection,
    // ProfileSection,
    PortSection,
    YoutubeSection,
    UnsplashSection,
    MovieSection,
  },
};
</script>
