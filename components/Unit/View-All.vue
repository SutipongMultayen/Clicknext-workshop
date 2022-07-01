<template>
  <div>
    <b-row>
      <b-col v-if="viewallShowTitle" class="text-title">{{ text }}</b-col>
      <b-col v-if="viewallShow" class="text-title" style="text-align: right">
        <span class="view-all"
          >ดูทั้งหมด <b-icon icon="arrow-right-circle" font-scale="1.2"></b-icon
        ></span>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
    },

    viewallShow: {
      type: Boolean,
      default: true,
    },
    viewallShowTitle: {
      type: Boolean,
      default: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.text-title {
  width: 99px;
  height: 40px;
  margin: 0 0 24px 0;
  font-size: 32px;
  font-weight: 500;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.25;
  letter-spacing: normal;
  color: #594f74;
}
.view-all {
  width: 65px;
  height: 24px;
  margin: 0 4px 4px 0;
  font-family: Tahoma;
  font-size: 16px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.5;
  letter-spacing: normal;
  color: #84848f;
}
</style>
