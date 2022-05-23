<template>
  <view class="app">
    <view class="introduce">
      <view class="introduce_title">
        <u-icon size="32" name="https://chen-1302611521.cos.ap-nanjing.myqcloud.com/icon.png" class="icon"></u-icon>
        <text>介绍</text>
      </view>
      <view class="introduce_content">
        那些更棒的点子来自于个体依然用过去习惯的方式思考创意时——坐在办公桌前时，在咖啡店等咖啡时，洗澡时。这些由人们独自想出的点子更胜一筹。当讨论会的狂热劲头散去，头脑风暴产生的点子其实并没有那么特别。
      </view>
      <slot></slot>
    </view>
  </view>
</template>

<script>
export default {
  name: "index",
}
</script>

<style lang="scss" scoped>
.app {
  margin: 0 26rpx;
  .introduce{
    margin: 48rpx 0;
    .introduce_title{
      display: flex;
      align-items: center;
      margin-bottom: 24rpx;
      .icon{
        margin-right: 16rpx;
      }
      text{
        font-size: 36rpx;
        font-weight: bold;
      }
    }
    .introduce_content{
      text-indent: 2em;
      font-size: 28rpx;
      line-height: 48rpx;
      margin-bottom: 48rpx;
    }
  }

}
</style>