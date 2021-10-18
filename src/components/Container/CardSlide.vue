<template>
  <swiper
    class="swiper-container"
    :slides-per-view="3"
    :space-between="50"
  >
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
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import SwiperCore, { Pagination } from 'swiper'

SwiperCore.use([Pagination])

@Component({
  components: {
    Swiper,
    SwiperSlide
  }
})
export default class extends Vue {}
</script>

<style lang="scss">
/* CARD CAROUSEL SLIDE */
.swiper-container {
  width: 100%;
  height: auto;
  overflow: hidden;

  .swiper-slide {
    /* Center slide text vertically */
    display: -webkit-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    flex-direction: column;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
    align-items: center;
  }

  .card {
    width: 100%;
    background-color: #f1f3f4;
    border-radius: 0.5rem;
    border: none;

    .card-image {
      display: block;
      width: 100%;
      height: 0;
      padding-top: calc(100% / 10 * 10);
      background-image: url("https://images.unsplash.com/photo-1609931424192-b7cf25773e26?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1170&q=80");
      background-size: cover;
      background-position: center;
      border-radius: 0.5rem 0.5rem 0 0;
    }

    .card-body {
      padding: 2rem 1.5rem;

      h2 {
        font-size: 1.5rem;
        font-weight: 900;
        margin-top: 0;
        margin-bottom: 1rem;

        p {
          font-size: 1rem;
          color: #747474;
          margin-block-end: 1rem;
        }

        a {
          display: table-cell;
          font-size: 1rem;
          font-weight: 600;
          color: #fff;
          padding: 0.75rem;
          border-radius: 0.5rem;
          background-color: $brandColor;
        }
      }
    }
  }
}

.swiper-pagination {
  bottom: 0.5rem;
  width: 100%;
  left: 0;
}

.swiper-pagination-bullet {
  width: 0.5rem;
  height: 0.5rem;
  margin-inline-start: 0.5rem;
}
</style>
