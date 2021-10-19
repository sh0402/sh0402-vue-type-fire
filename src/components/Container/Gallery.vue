<template>
  <div class="gallery-box col-lg-6">
    <div class="gallery-filter"></div>
    <img :src="GalleryData.image" alt="" />
    <div class="content-element">
      <h4>{{ GalleryData.title }}</h4>
      <p>{{ GalleryData.subTitle }}</p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  props: {
    GalleryData: Array
  }
})
</script>
