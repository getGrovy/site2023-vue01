<template>
  <ContTitle title="unsplash" />
  <UnsplashSlider />
  <UnsplashSearch />
  <UnsplashTag />
  <UnsplashCont :unsplashs="unsplash" />
</template>
<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import UnsplashSearch from "@/components/unsplash/UnsplashSearch.vue";
import UnsplashSlider from "@/components/unsplash/UnsplashSlider.vue";
import UnsplashTag from "@/components/unsplash/UnsplashTag.vue";
import UnsplashCont from "@/components/unsplash/UnsplashCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    UnsplashSlider,
    UnsplashSearch,
    UnsplashTag,
    UnsplashCont,
  },

  setup() {
    //setup()으로 넣어야함
    const unsplash = ref([]);
    const TopunSplash = async () => {
      await fetch(
        "https://api.unsplash.com/photos?client_id=pFw6Wg1LihMi6bDCtjKqXkXBB73nebE4T2kBp6b26RE&per_page	=30"
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result);
          unsplash.value = result;
        })
        .catch((error) => console.log("error", error));
      console.log(unsplash);
    };
    TopunSplash();
    return {
      TopunSplash,
      unsplash,
    };
  },
};
</script>
