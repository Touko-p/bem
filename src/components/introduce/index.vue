<template>
  <view class="ht-main">
    <view class="ht-main__introduce">
      <view class="ht-main__introduce--title">
        <u-icon size="32" name="https://chen-1302611521.cos.ap-nanjing.myqcloud.com/icon.png" class="ht-main__introduce--icon"></u-icon>
        <text>介绍</text>
      </view>
      <view class="ht-main__introduce--content">
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
@import "../../assets/scss/bem.scss";
@include block(main){
  margin: 0 26rpx;
  @include element(introduce){
    margin: 48rpx 0;
    @include modifier(title){
      display: flex;
      align-items: center;
      margin-bottom: 24rpx;
    }
    @include modifier(content){
      text-indent: 2em;
      font-size: 28rpx;
      line-height: 48rpx;
      margin-bottom: 48rpx;
    }
    @include modifier(icon){
      margin-right: 16rpx;
    }
  }
}


text{
  font-size: 36rpx;
  font-weight: bold;
}

</style>