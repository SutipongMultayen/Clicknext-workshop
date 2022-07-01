<template>
  <div>
    <script src="https://unpkg.com/flickity@2/dist/flickity.pkgd.min.js"></script>
    <link
      rel="stylesheet"
      href="https://unpkg.com/flickity@2/dist/flickity.min.css"
    />
    <!-- Flickity HTML init -->
    <ViewAll text="Set Index" :viewallShowTitle="false"/>
    <div
      class="carousel"
      data-flickity='{ "cellAlign": "left", "groupCells": "3", "imagesLoaded": true, "prevNextButtons": false, "pageDots": true }'
    >
      <div class="m-2">
        <img src="@/assets/img/021A83E8.png" class="p-3 w-100" />
        <div class="p-3 w-75">
          <span class="KKP-Focus-2"> KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม </span>
        </div>
      </div>
      <div class="m-2">
        <img src="@/assets/img/3AE32842.png" class="p-3 w-100" />
        <div class="p-3 w-75">
          <span class="KKP-Focus-2">
            KKP Focus ช่วงที่ 1 ย่อประเด็นโลก โยกประเด็นร้อน
          </span>
        </div>
      </div>
      <div class="m-2">
        <img src="@/assets/img/99062220.png" class="p-3 w-100" />
        <div class="p-3 w-75">
          <span class="KKP-Focus-2">KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม </span>
        </div>
      </div>
      <div class="m-2">
        <img src="@/assets/img/021A83E8.png" class="p-3 w-100" />
        <div class="p-3 w-75">
          <span class="KKP-Focus-2">KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม </span>
        </div>
      </div>
      <div class="m-2">
        <img src="@/assets/img/934C8FF6.png" class="p-3 w-100" />
        <div class="p-3 w-75">
          <span class="KKP-Focus-2">KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม </span>
        </div>
      </div>
      <div class="m-2">
        <img src="@/assets/img/021A83E8.png" class="p-3 w-100" />
        <div class="p-3 w-75">
          <span class="KKP-Focus-2">KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม </span>
        </div>
      </div>
      <div class="m-2">
        <img src="@/assets/img/934C8FF6.png" class="p-3 w-100" />
        <div class="p-3 w-75">
          <span class="KKP-Focus-2">KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม </span>
        </div>
      </div>
      <div class="m-2">
        <img src="@/assets/img/021A83E8.png" class="p-3 w-100" />
        <div class="p-3 w-75">
          <span class="KKP-Focus-2"> KKP Focus ช่วงที่ 2 กูรู... โต๊ะกลม </span>
        </div>
      </div>
      <!-- <img src="@/assets/img/99062220.png" class="pl-2" />
      <img src="@/assets/img/934C8FF6.png" class="pl-2" />
      <img src="@/assets/img/3E62407F.png" class="pl-2" />
      <img src="@/assets/img/934C8FF6.png" class="pl-2" />
      <img src="@/assets/img/021A83E8.png" class="pl-2" />
      <img src="@/assets/img/3AE32842.png" class="pl-2" />
      <img src="@/assets/img/99062220.png" class="pl-2" />
      <img src="@/assets/img/934C8FF6.png" class="pl-2" />
      <img src="@/assets/img/3E62407F.png" class="pl-2" />
      <img src="@/assets/img/934C8FF6.png" class="pl-2" /> -->
    </div>
  </div>
</template>

<script>
import ViewAll from '@/components/Unit/View-All'
export default {
  components: { ViewAll },
}
</script>

<style lang="scss" scoped>
/* external css: flickity.css */

* {
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
}

/* force scrollbar, not necessary, but may reduce gaps. Setting a max-height on .carousel also works */
html {
  overflow-y: scroll;
}

.carousel {
  background: #fff;
  // width: 300px;
}

.carousel img {
  display: block;
  height: 275px;
}

.KKP-Focus-2 {
  width: 314px;
  height: 90px;
  // padding-left: 0.5rem !important;
  font-family: Kanit;
  font-size: 24px;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #594f74;
}
</style>
