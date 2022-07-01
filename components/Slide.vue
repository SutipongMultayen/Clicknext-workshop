<template>
  <div class="arousel-bg">
    <!-- slide  -->
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="7000"
      controls
      background="#ababab"
      img-width="1024"
      img-height="650"
      style="text-shadow: 1px 1px 2px #333"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Slides with custom text -->
      <b-carousel-slide
        img-src="@/assets/img/531B48BF58B2.png"
        class="img-fluid-custom"
        style="height: 650px"
      ></b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide
        img-src="@/assets/img/crito.jpg"
        class="img-fluid-custom"
        style="height: 650px"
      ></b-carousel-slide>
    </b-carousel>

    <!-- slide-small  -->
    <div class="px-5" style="position: relative; bottom: 41px">
      <div id="slider-container" class="slider">
        <div
          v-for="(item, index) in slidingSmall"
          :key="index"
          class="slide-small px-1"
        >
          <div
            :class="[
              { 'Rectangle-2-Copy-3': btnActive != `btn${index}` },
              { 'Rectangle-Active': btnActive == `btn${index}` },
            ]"
            @click="btnActive = `btn${index}`"
          >
            <span
              :class="[
                'Rectangle-text',
                { 'text-light': btnActive == `btn${index}` },
              ]"
            >
              {{ item }}
            </span>
            <div class="Rectangle"></div>
          </div>
        </div>

        <div @click="prev()" class="control-prev-btn">
          <b-icon icon="chevron-left" font-scale="3"></b-icon>
        </div>
        <div @click="next()" class="control-next-btn">
          <b-icon icon="chevron-right" font-scale="3"></b-icon>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null,
      slidingSmall: [
        'About Us',
        'Awards',
        'Our Businesses',
        'News Activities',
        'News 1',
      ],
      btnActive: 'btn0',
    }
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    },
    prev() {
      document.getElementById('slider-container').scrollLeft -= 303
    },

    next() {
      document.getElementById('slider-container').scrollLeft += 303
    },
  },
}
</script>

<style lang="scss" scoped>
.arousel-bg {
  background-color: #f3f4f7;
}
// --- slide
.carousel {
  height: 650px;
}

// ------------------
.slider {
  display: flex;
  // height: 350px;
  margin-left: 18%;
  margin-right: 18%;
  max-height: auto;
  overflow-y: hidden;
  overflow-x: scroll !important;
  padding: 16px;
  transform: scroll(calc(var(--i, 0) / var(--n) * -100%));
  scroll-behavior: smooth;
}
.slider::-webkit-scrollbar {
  height: 5px;
  width: 150px;
  display: none;
}
.slider::-webkit-scrollbar-track {
  background: transparent;
}
.slider::-webkit-scrollbar-thumb {
  background: #888;
}
.slider::-webkit-scrollbar-thumb:hover {
  background: #555;
}
.slider img:hover {
  transform: scale(1.05);
  box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.15);
}
.slide-small {
  position: relative;
}

.control-prev-btn {
  position: absolute;
  top: 34%;
  left: 14%;
  height: 100px;
  line-height: 100px;
  width: 45px;
  text-align: center;
  user-select: none;
  color: #444;
  cursor: pointer;
  z-index: 1;
}
.control-next-btn {
  position: absolute;
  top: 34%;
  right: 14%;
  height: 100px;
  line-height: 100px;
  width: 45px;
  text-align: center;
  user-select: none;
  color: #444;
  cursor: pointer;
  z-index: 1;
}
.overlay {
  position: absolute;
  height: 100%;
  width: 100%;
  background: rgba(0, 0, 0, 0.45);
  top: 0;
  display: none;
}
.overlay.active {
  display: block;
}
@media only screen and (max-width: 420px) {
  .slider {
    padding: 0;
  }
  .slide-small {
    padding: 16px 10px;
  }
  .control-prev-btn {
    top: 37%;
  }
  .control-next-btn {
    top: 37%;
  }
}
// ----------------------

.Rectangle-2-Copy-3 {
  width: 262px;
  height: 86px;
  margin: 0 8px 0 9px;
  padding: 28px 0 0;
  border-radius: 2px;
  background-image: linear-gradient(
    to right,
    #eeedf2 3%,
    #ebeaef 34%,
    #e5e5e8 94%
  );
  cursor: pointer;
}

.Rectangle-Active {
  width: 262px;
  height: 86px;
  margin: 0 8px 0 9px;
  padding: 28px 0 0;
  border-radius: 2px;
  color: #fff;
  background-image: linear-gradient(to left, #655a9f, #8b8bc1);
  cursor: pointer;
}

.Rectangle {
  width: 262px;
  height: 7px;
  margin: 21px 0 0;
  background-image: linear-gradient(to right, #8c8bc2 4%, #64599e);
}

.Rectangle-text {
  width: 150px;
  height: 30px;
  margin: 0 86px 21px 26px;
  font-family: Kanit;
  font-size: 20px;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: normal;
  color: #594f74;
}
</style>
