<template>
  <view class="item">
    <view class="item_header">
      <view class="item_header_tag">

      </view>
      <text class="item_header_text">
        {{ title }}
      </text>
    </view>
    <slot>
      <u-image src="@/assets/images/2.jpg" mode="widthFix"></u-image>
      <view class="item_connect">
        <u-icon size="28" name="https://chen-1302611521.cos.ap-nanjing.myqcloud.com/phone.png" class="icon"></u-icon>
        <text class="item_connect_phone">
          电话：{{ phone }}
        </text>
        <button class="mini-btn" type="default" size="mini" @click="consultNow(phone)">咨询</button>
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
$namespace:"item";

@include block(main){ //==> .item-header
  color: red;

  @include element(tag){ // ==> .item-header__tag
    width: 100px;
    height: 100px;
    background-color: #4cd964;
    @include modifier(app) { // ==> .item-header__tag--app

    }
    @include modifier(web) { // ==> .item-header__tag--web

    }
    @include state(selected){// ==> .item-main__tag  is-selected
      color: #333333;
    }

  }

}

.item{
  margin-bottom: 24rpx;
  .item_header{
    display: flex;
    align-items: center;
    margin-bottom: 32rpx;
    .item_header_tag{
      width: 8rpx;
      height: 28rpx;
      background: #5F9F76;
      border-radius: 6rpx;
      margin-right: 24rpx;
    }
    .item_header_text{
      font-size: 32rpx;
      font-weight: bold;
    }
  }
  .item_connect{
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 32rpx;
    margin-top: 24rpx;
    .item_connect_phone{
      margin: 0 20rpx 0 8rpx;
    }
  }
}
.mini-btn{
  background: #FF8504;
  color: #fff;
  margin: 0;
}
</style>