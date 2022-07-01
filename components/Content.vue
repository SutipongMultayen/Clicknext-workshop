<!-- Please remove this file from your project -->
<template>
  <div>
    <div id="bg-img">
      <div class="content-set-lr">
        <div class="bv-example-row">
          <b-row>
            <b-col cols="12" sm="8">
              <ViewAll text="Article" />
              <b-row>
                <b-col>
                  <img src="@/assets/img/EF7E37D9.png" class="img_article1" />
                </b-col>
                <b-col>
                  <div class="article1">
                    <span class="Margin-of-Safety-Copy">
                      Margin of Safety กลยุทธ์การลงทุนอย่างปลอดภัย
                      หลักการลงทุนของเบนจามิน เกรแฮม
                    </span>
                  </div>
                  <div>
                    <span class="\-">
                      ตอบคำถามที่ว่า คุณมีความจำเป็น พร้อมเป็นเจ้าของหรือยัง
                      เช่น เพื่อหน้าที่การงาน อาชีพ หรือการเดินทาง ความสะดวกสบาย
                      เพราะการซื้อรถนอกจากค่ารถแล้ว ยังมีค่าน้ำมัน ค่าบำรุงรักษา
                      ค่าประกันภัย ซึ่งเป็นค่าใช้จ่ายในระยะยาว
                    </span>
                  </div>
                  <div class="Rectangle-4">การลงทุน</div>
                </b-col>
              </b-row>
            </b-col>
            <b-col cols="12" sm="4">
              <ViewAll text="News" />
              <CarouselSlideshow />
            </b-col>
          </b-row>

          <b-row cols="1" cols-sm="3" cols-lg="3">
            <b-col>
              <img src="@/assets/img/934C8FF6.png" class="img_article1" />
              <div>
                <span class="Margin-of-Safety-Copy article1">
                  จับจังหวะการลงทุนเป็นก็สร้างเงินล้านได้ง่ายๆใกล้แค่เอื้อม
                </span>
              </div>
              <div class="Rectangle-4">การลงทุน</div>
            </b-col>
            <b-col>
              <img src="@/assets/img/3E62407F.png" class="img_article1" />
              <div>
                <span class="Margin-of-Safety-Copy article1">
                  Margin of Safety กลยุทธ์การลงทุนอย่างปลอดภัย Margin of Safety
                </span>
              </div>
              <div class="Rectangle-4">การลงทุน</div>
            </b-col>
            <b-col>
              <div class="Rectangle">
                <ViewAll text="Set Index" :viewallShow="false" />
                <img src="@/assets/img/A69442DB.png" />
              </div>
            </b-col>
          </b-row>
        </div>
      </div>
    </div>

    <!-- //! KKP Channel -->
    <div class="position-relative" style="margin: 72px 0px;">
      <div class="Line-3-Copy-6"></div>
      <span class="KKP-Channel"> KKP Channel </span>
      <span class="KKP-Channel-text">
        อัปเดตทุกความรู้ด้านการเงินและการลงทุนก่อนใคร
        พร้อมอินเทรนด์ไปกับหลากหลายเรื่องราวไลฟ์สไตล์
      </span>
    </div>

    <div class="content-set-lr">
      <Tabsvedio />
      <div>
        <SlideGroup />
      </div>
    </div>
  </div>
</template>

<script>
// https://codepen.io/abhishekdana/pen/zYYXbMY
// https://css-tricks.com/css-only-carousel/
import ViewAll from '@/components/Unit/View-All'
import Tabsvedio from '@/components/Tabs-vedio'
import CarouselSlideshow from '@/components/Unit/carousel-slideshow'
import SlideGroup from '@/components/Unit/Slide-Group'
export default {
  name: 'NuxtTutorial',
  components: { ViewAll, CarouselSlideshow, Tabsvedio, SlideGroup },
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
  methods: {},
}
</script>

<style lang="scss" scoped>
#bg-img {
  clip-path: polygon(0 0, 100% 0, 100% 91%, 65% 96%, 0 100%);
  background-color: #f3f4f7;
  // width: 1366px;
  // height: 1073px;
  width: 100%;
  height: 974px;
  max-height: 1073px;
  // margin: 581px 0 43px;
  // padding: 126px 98px 136px;
  object-fit: contain;
  // background-image: url('@/assets/img/FC8B44A9.png');
}
.content-set-lr {
  margin: 0 275px;
}

img.img_article1 {
  width: 428px;
  height: 298px;
  margin: 26px 27px 15px 0;
  object-fit: contain;
}

.Margin-of-Safety-Copy {
  width: 303px;
  height: 90px;
  // margin: 26px 42px 17px 0px;
  font-family: Kanit;
  font-size: 30px;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #594f74;
}
CSS .\- {
  width: 315px;
  height: 120px;
  margin: 17px 30px 33px 27px;
  font-family: Tahoma;
  font-size: 16px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: normal;
  color: #84848f;
}

.Rectangle-4 {
  border-left: 3px solid #635f98;
  height: 17px;
  font-family: Tahoma;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.2;
  letter-spacing: normal;
  color: #635f98;
  padding: 0 8px;
  margin: 33px 0 0 0;
}

.Rectangle {
  width: 370px;
  height: 368px;
  margin: 36px 0 0 29px;
  padding: 10px 32px 21px 43px;
  background-color: #fff;
}

.Line-3-Copy-6 {
  width: 52px;
  height: 3px;
  margin: 0 55px 0px 0;
  border-style: solid;
  border-width: 3px;
  border-image-source: linear-gradient(to right, #e9eaef -18%, #b9b9c3 122%);
  border-image-slice: 1;
  position: absolute;
  top: 40%;
  left: 14%;
}

.KKP-Channel {
  width: 193px;
  height: 40px;
  margin: 43px 33px 69px 337px;
  font-family: Kanit;
  font-size: 32px;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #594f74;
}

span .KKP-Channel-text {
  width: 847px;
  height: 26px;
  margin: 55px 125px 71px 26px;
  font-family: Kanit;
  font-size: 18px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.44;
  letter-spacing: normal;
  color: #84848f;
}
</style>
