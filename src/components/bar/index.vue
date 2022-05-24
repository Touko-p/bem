<template>
  <view class="ht-bar">
    <button class="ht-bar__button" type="default" @click="consultNow">立即咨询</button>
    <button class="ht-bar__button is-active" type="default">获取更多</button>
  </view>
</template>

<script lang="ts">
export default {
  name: "index",
  methods:{
    consultNow(){
      uni.makePhoneCall({
        phoneNumber: '114' //仅为示例
      });
    }
  }
}
</script>

<style lang="scss" scoped>
$primary:#5F9F76;
@import "../../assets/scss/bem.scss";
@include block(bar){
  width: 100%;
  height: 112rpx;
  background: #fff;
  position: fixed;
  bottom: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  @include element(button){
    width: 320rpx;
    height: 72rpx;
    line-height: 72rpx;
    color: $primary;
    border:2rpx solid $primary;
    @include state(active){
      background:$primary ;
      color: #fff !important;
    }
  }
}
</style>