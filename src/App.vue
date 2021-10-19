<template>
  <div id="app">
    <Navi />
    <div class="container">
      <router-view :GalleryData="GalleryData"/>
    </div>
    <Footer />
  </div>
</template>

<script>
import { Component, Vue } from 'vue-property-decorator'
import Navi from '@/components/Head/Navi.vue'
import Footer from '@/components/Foot/Footer.vue'
import GalleryData from '@/assets/data/galleryData.js'

@Component({
  components: {
    Navi,
    Footer
  },
  data () {
    return {
      GalleryData: GalleryData
    }
  }
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import '@/assets/styles/_variabled.scss';
@import '@/assets/styles/scss/common.scss';
@import '@/assets/styles/scss/header.scss';
@import '@/assets/styles/scss/footer.scss';
@import '@/assets/styles/scss/home.scss';
@import '@/assets/styles/scss/about.scss';
@import '@/assets/styles/scss/contact.scss';

#app {
  font-family: Roboto, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 6rem;
  display: flex;
  flex-direction: column;
  // margin-bottom: 12rem;
}

</style>
