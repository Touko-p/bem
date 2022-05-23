<template>
  <view class="bar">
    <button class="bar_button1" type="default" @click="consultNow">立即咨询</button>
    <button class="bar_button2" type="default">获取更多</button>
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
.bar{
  width: 100%;
  height: 112rpx;
  background: #fff;
  position: fixed;
  bottom: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  button{
    width: 320rpx;
    height: 72rpx;
    line-height: 72rpx;
  }
  .bar_button1{
    color: $primary;
    border:2rpx solid $primary;
  }
  .bar_button2{
    background:$primary ;
    color: #fff;
  }
}
</style>