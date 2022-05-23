<template>
  <view class="info">
    <view class="info_title">
      {{ title }}
    </view>
    <u-image src="@/assets/images/2.jpg" mode="widthFix"></u-image>
  </view>
</template>

<script lang="ts">
export default {
  name: "index",
  props:{
    title:String
  }
}
</script>

<style lang="scss" scoped>
.info{
  margin-bottom: 32rpx;
  .info_title{
    font-size: 30rpx;
    margin-bottom: 16rpx;
  }
}
</style>