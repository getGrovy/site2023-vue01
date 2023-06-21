<template>
  <div className="unsplash__cont container">
    <ul>
      <li v-for="(image, index) in unsplashs" :key="index">
        <a :href="`https://unsplash.com/photos/${image.id}`">
          <img :src="`${image.urls.small}`" :alt="`${image.alt_description}`" />
          <em>
            <span class="start">{{ image.alt_description }}</span>
          </em>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    unsplashs: {
      type: Array,
      required: true,
    },
  },
};
</script>
