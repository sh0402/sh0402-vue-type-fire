<template>

  <div class="wrapper">
    <swiper
     :options="SwiperOptions"
      class="swiper-container"
    >
      <swiper-slide :style="width=20">
        <div class="card swiper-slide">
          <div class="card-image"></div>
          <div class="card-body">
            <h2>work-class-name</h2>
            <p>
              Adobe Photoshop & illustrator Working Time : 4 Days<br />
              Size : 1,020 x 1,020 x 460 (mm)
            </p>
            <a href="#" class="btn btn-primary"> Lead More </a>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card swiper-slide">
          <div class="card-image"></div>
          <div class="card-body">
            <h2>work-class-name</h2>
            <p>
              Adobe Photoshop & illustrator Working Time : 4 Days<br />
              Size : 1,020 x 1,020 x 460 (mm)
            </p>
            <a href="#" class="btn btn-primary"> Lead More </a>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card swiper-slide">
          <div class="card-image"></div>
          <div class="card-body">
            <h2>work-class-name</h2>
            <p>
              Adobe Photoshop & illustrator Working Time : 4 Days<br />
              Size : 1,020 x 1,020 x 460 (mm)
            </p>
            <a href="#" class="btn btn-primary"> Lead More </a>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card swiper-slide">
          <div class="card-image"></div>
          <div class="card-body">
            <h2>work-class-name</h2>
            <p>
              Adobe Photoshop & illustrator Working Time : 4 Days<br />
              Size : 1,020 x 1,020 x 460 (mm)
            </p>
            <a href="#" class="btn btn-primary"> Lead More </a>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="card swiper-slide">
          <div class="card-image"></div>
          <div class="card-body">
            <h2>work-class-name</h2>
            <p>
              Adobe Photoshop & illustrator Working Time : 4 Days<br />
              Size : 1,020 x 1,020 x 460 (mm)
            </p>
            <a href="#" class="btn btn-primary"> Lead More </a>
          </div>
        </div>
      </swiper-slide>
    </swiper>
    <div class="swiper-pagination" slot="pagination"></div>
  </div>

</template>

<script lang="ts">
// import { Component, Vue } from 'vue-property-decorator'
// // import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
// import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
// import SwiperCore, { Pagination } from 'swiper'

// SwiperCore.use([Pagination])

// @Component({
//   components: {
//     Swiper,
//     SwiperSlide
//   },
//   data () {
//     return {
//       SwiperOptions: {
//         slidesPerView: 2.5,
//         spaceBetween: 10,
//         pagination: {
//           el: '.swiper-pagination',
//           clickable: true
//         }
//       }
//     }
//   }
// })
// export default class CardSlide extends Vue {}
import { defineComponent } from '@vue/composition-api'
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'

export default defineComponent({
  components: {
    Swiper,
    SwiperSlide
  },
  data () {
    return {
      SwiperOptions: {
        slidesPerView: 2.5,
        spaceBetween: 10,
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        }
      }
    }
  }
})
</script>

<style lang="scss"></style>
