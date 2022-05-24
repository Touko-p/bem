<template>
  <view class="ht-main">
    <view class="ht-main__title">
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
@import "../../assets/scss/bem.scss";
@include block(main){
  margin-bottom: 32rpx;
  @include element(title){
    font-size: 30rpx;
    margin-bottom: 16rpx;
  }
}
</style>