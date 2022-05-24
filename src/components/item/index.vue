<template>
  <view class="ht-main">
    <view class="ht-main__header">
      <view>

      </view>
      <text>
        {{ title }}
      </text>
    </view>
    <slot>
      <u-image src="@/assets/images/2.jpg" mode="widthFix"></u-image>
      <view class="ht-main__content">
        <u-icon size="28" name="https://chen-1302611521.cos.ap-nanjing.myqcloud.com/phone.png" class="icon"></u-icon>
        <text>
          电话：{{ phone }}
        </text>
        <button class="ht-main__btn" type="default" size="mini" @click="consultNow(phone)">咨询</button>
      </view>
    </slot>
  </view>
</template>

<script lang="ts">
export default {
  name: "index",
  props:{
    title:String,
    phone:Number
  },
  methods:{
    consultNow(phone:number){
      uni.makePhoneCall({
        phoneNumber: '114' //仅为示例
      });
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../../assets/scss/bem.scss";

@include block(main){ //==> .ht-main
  margin-bottom: 24rpx;
  @include element(header){ // ==> .ht-main__header
    display: flex;
    align-items: center;
    margin-bottom: 32rpx;
    text{
      font-size: 32rpx;
      font-weight: bold;
    }
    view{
      width: 8rpx;
      height: 28rpx;
      background: #5F9F76;
      border-radius: 6rpx;
      margin-right: 24rpx;
    }
    @include state(selected){// ==> .ht-main__tag  is-selected
      color: #333333;
    }

  }
  @include element(content){
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 32rpx;
    margin-top: 24rpx;
    text{
      margin: 0 20rpx 0 8rpx;
    }
  }
  @include element(btn){
    background: #FF8504;
    color: #fff;
    margin: 0;
  }
}
</style>