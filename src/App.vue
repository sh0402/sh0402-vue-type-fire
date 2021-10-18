<template>
  <div id="app">
    <Navi />
    <div class="container"><router-view/></div>
    <Footer />
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'
import Navi from '@/components/Head/Navi.vue'
import Footer from '@/components/Foot/Footer.vue'
import GalleryData from '@/assets/data/galleryData'

export default defineComponent({
  components: {
    Navi,
    Footer
  },
  data () {
    return {
      GalleryData: GalleryData
    }
  },
  setup () {
    ///
  }
})
</script>

<style lang="scss">
@import '@/assets/styles/_variabled.scss';
@import '@/assets/styles/scss/common.scss';
@import '@/assets/styles/scss/header.scss';
@import '@/assets/styles/scss/footer.scss';
@import '@/assets/styles/scss/home.scss';

#app {
  font-family: Roboto, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 6rem;
}

</style>
