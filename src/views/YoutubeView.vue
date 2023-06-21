<template>
  <ContTitle title="YOUTUBE" />
  <YoutubeSearch />
  <YoutubeSlider />
  <YoutubeTag />
  <YoutubeCont :youtubes="youtube" />
</template>
<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import YoutubeSearch from "@/components/youtube/YoutubeSearch.vue";
import YoutubeSlider from "@/components/youtube/YoutubeSlider.vue";
import YoutubeTag from "@/components/youtube/YoutubeTag.vue";
import YoutubeCont from "@/components/youtube/YoutubeCont.vue";
import { ref } from "vue";
export default {
  components: {
    ContTitle,
    YoutubeSlider,
    YoutubeSearch,
    YoutubeTag,
    YoutubeCont,
  },
  setup() {
    //setup()으로 넣어야함
    const youtube = ref([]);
    const TopYoutube = async () => {
      await fetch(
        // "https://www.googleapis.com/youtube/v3/videos?id=7lCDEYXw3mM&key=AIzaSyBmD-yNiyzU1muLrsF_Gg7FKf5HgyXfxlo&part=snippet,contentDetails,statistics,status"
        "https://youtube.googleapis.com/youtube/v3/search?part=snippet&maxResults=30&q=로스트아크&key=AIzaSyBmD-yNiyzU1muLrsF_Gg7FKf5HgyXfxlo"
        // AIzaSyBmD-yNiyzU1muLrsF_Gg7FKf5HgyXfxlo
      )
        .then((response) => response.json())
        .then((result) => {
          console.log(result.items);
          youtube.value = result.items;
        })
        .catch((error) => console.log("error", error));
      console.log(youtube);
    };
    TopYoutube();
    return {
      TopYoutube,
      youtube,
    };
  },
};
</script>
