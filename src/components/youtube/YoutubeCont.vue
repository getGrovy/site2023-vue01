<template>
  <div className="youtube__cont container">
    <ul>
      <li v-for="(data, index) in youtubes" :key="index">
        <a :href="`https://www.youtube.com/watch?v=${data.id.videoId}`">
          <img
            :src="data.snippet.thumbnails.medium.url"
            :alt="data.snippet.title"
          />
          <em>
            <span class="start">{{ data.snippet.title }}</span>
          </em>
        </a>

        <em>
          <!-- <span class="title">{{ data.title }}</span> -->
          <!-- <span class="start">{{ data.vote_average }}</span> -->
        </em>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    youtubes: {
      type: Array,
      required: true,
    },
  },
};
</script>
