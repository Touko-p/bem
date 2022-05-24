<template>
  <view :class="showBar ? 'bar_show' : 'bar_hidden'">
    <view>
      <u-image src="@/assets/images/2.jpg" mode="widthFix"></u-image>
    </view>
    <slot></slot>
  </view>
</template>

<script lang="ts">
export default {
  name: "index",
  props:{
    showBar:false
  },
  data() {
    return {}
  }
}
</script>

<style lang="scss" scoped>
.bar_show{
  padding-bottom: 112rpx;
}
.bar_hidden{
  padding-bottom: 56rpx;
}
</style>