<template>
  <ContTitle title="unsplash" />
  <UnsplashSlider :images="images" />
  <!-- <UnsplashSearch /> -->
  <!-- <UnsplashTag /> -->
  <UnsplashCont :images="images" />
</template>

<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import UnsplashSlider from "@/components/unsplash/UnsplashSlider.vue";
// import UnsplashSearch from "@/components/unsplash/UnsplashSearch.vue";
// import UnsplashTag from "@/components/unsplash/UnsplashTag.vue";
import UnsplashCont from "@/components/unsplash/UnsplashCont.vue";

import { ref } from "vue";

export default {
  components: {
    ContTitle,
    UnsplashSlider,
    // UnsplashSearch,
    // UnsplashTag,
    UnsplashCont,
  },

  setup() {
    const images = ref([]);

    const TopImages = async () => {
      await fetch(
        "https://api.unsplash.com/photos?client_id=J2LaT4yhkYj1aMevZIbcACiyXSt2ATNj11PIfnxis9M&per_page=30"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result);
          images.value = result;
        })
        .catch((error) => console.log("error", error));
    };
    TopImages();

    return {
      images,
      TopImages,
    };
  },
};
</script>
