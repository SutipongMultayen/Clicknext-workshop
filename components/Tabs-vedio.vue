<template>
  <div>
    <b-row>
      <b-col>
        <b-row>
          <span
            :class="[btnActive == 'btn0' ? 'KKP-FOCUS' : 'KKP-Advisor']"
            @click="btnActive = `btn0`"
          >
            KKP FOCUS
          </span>
          <div class="Line-7"></div>

          <span
            :class="[btnActive == 'btn1' ? 'KKP-FOCUS' : 'KKP-Advisor']"
            @click="btnActive = `btn1`"
            >OPTIMISE</span
          >
          <div class="Line-7"></div>

          <span
            :class="[btnActive == 'btn2' ? 'KKP-FOCUS' : 'KKP-Advisor']"
            @click="btnActive = `btn2`"
            >KKP Advisor</span
          >
          <div class="Line-7"></div>
        </b-row>
      </b-col>
    </b-row>

    <div>
      <b-row v-if="btnActive == 'btn0'">
        <b-col>
          <b-embed
            type="iframe"
            aspect="16by9"
            src="https://www.youtube.com/embed/zpOULjyy-n8?rel=0"
            allowfullscreen
          ></b-embed>
        </b-col>

        <b-col>
          <div class="Line-4-Copy-2"></div>
          <span class="KKP-Focus"> KKP Focus </span>
          <div class="w-50" style="margin: 0 0 0 54px">
            <span class="text-KKP-Focus">
              ฝนนักสู้ พบเรื่องราวจริง เจ็บจริง ประสบความสำเร็จจริง
              ที่จะเป็นแรงกระตุ้นให้ SME นักสู้รุ่นต่อไป ได้ก้าวไปถึงฝัน
            </span>
          </div>
          <div class="Line-4-Copy"></div>
        </b-col>
      </b-row>
      <b-row v-if="btnActive == 'btn1'">
        <b-col>
          <b-embed
            type="iframe"
            aspect="16by9"
            src="https://www.youtube.com/embed/fJ9rUzIMcZQ"
            allowfullscreen
          ></b-embed>
        </b-col>

        <b-col>
          <div class="Line-4-Copy-2"></div>
          <span class="KKP-Focus">OPTIMISE</span>
          <div class="w-50" style="margin: 0 0 0 54px">
            <span class="text-KKP-Focus">
              REMASTERED IN HD TO CELEBRATE ONE BILLION VIEWS! Taken from A
              Night At The Opera, 1975.
            </span>
          </div>
          <div class="Line-4-Copy"></div>
        </b-col>
      </b-row>
      <b-row v-if="btnActive == 'btn2'">
        <b-col>
          <b-embed
            type="iframe"
            aspect="16by9"
            src="https://www.youtube.com/embed/kijpcUv-b8M"
            allowfullscreen
          ></b-embed>
        </b-col>

        <b-col>
          <div class="Line-4-Copy-2"></div>
          <span class="KKP-Focus">KKP Advisor</span>
          <div class="w-50" style="margin: 0 0 0 54px">
            <span class="text-KKP-Focus">
              Taken from A Day At The Races, 1976 and Forever, 2014. Queen-
              Somebody To Love (promo video, 1976)
            </span>
          </div>
          <div class="Line-4-Copy"></div>
        </b-col>
      </b-row>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      btnActive: 'btn0',
    }
  },
}
</script>

<style lang="scss" scoped>
.KKP-FOCUS {
  // width: 126px;
  height: 30px;
  margin: 3px 33px 2px 0;
  font-family: Kanit;
  font-size: 24px;
  font-weight: 700;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #594f74;
  cursor: pointer;
}

.KKP-Advisor {
  // width: 102px;
  height: 30px;
  margin: 3px 33px 2px 0;
  font-family: Kanit;
  font-size: 24px;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #84848f;
  cursor: pointer;
}

.Line-7 {
  width: 3px;
  height: 23px;
  margin: 5px 43px 7px 33px;
  border: solid 1px #adacb9;
}

.embed-responsive {
  margin: 29px 0px;
}

.Line-4-Copy-2 {
  width: 266px;
  height: 3px;
  margin: 64px 19px 64px 44px;
  border-style: solid;
  border-width: 3px;
  border-image-source: linear-gradient(
    to right,
    #d0cfd8 -3%,
    #e9eaef 55%,
    #b9b9c3 111%
  );
  border-image-slice: 1;
}

.KKP-Focus {
  width: 266px;
  height: 63px;
  margin: 64px 13px 14px 50px;
  font-family: Kanit;
  font-size: 42px;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: normal;
  color: #594f74;
}

.text-KKP-Focus {
  width: 276px;
  height: 112px;
  // margin: 14px 0 76px 53px;
  font-family: Kanit;
  font-size: 20px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.4;
  letter-spacing: normal;
  color: #84848f;
}

.Line-4-Copy {
  width: 266px;
  height: 3px;
  margin: 76px 19px 42px 44px;
  border-style: solid;
  border-width: 3px;
  border-image-source: linear-gradient(
    to right,
    #d0cfd8 -3%,
    #e9eaef 55%,
    #b9b9c3 111%
  );
  border-image-slice: 1;
}
</style>
