<template>
  <view>
    <block v-for="(v,k) in list" :key="k">
      <button type="default" @click="jump(v)">立即跳转page{{k+1}}</button>
    </block>
  </view>
</template>

<script lang="ts">
type data = {
  url:string,
  data:object
};
import Vue from 'vue';
import allPage from "@/components/allPage/index.vue";
export default Vue.extend({
  components: {
    allPage
  },
  data() {
    return {
      list: [
        {
          url: "/pages/page1/index",
          data:{
            value1:[
              {
                title:'武汉',
                phone:123456780468
              },
              {
                title:'贵阳',
                phone:123456780468
              },
              {
                title:'海南',
                phone:123456780468
              },
            ],
            showBar:false
          }
        },
        {
          url: "/pages/page1/index",
          data:{
            value1:[
              {
                title:'娱乐项目'
              }
            ],
            value2:[
              '棋牌室','茶艺室'
            ],
            showBar:true
          }
        },
        {
          url: "/pages/page1/index",
          data:{
            value1:[
              {
                title:'活动介绍'
              }
            ],
            value2:[
              '活动一','活动二'
            ],
            showBar:true
          }
        }
      ]
    }
  },
  onLoad() {

  },
  methods: {
    jump(value:data) {
      uni.navigateTo({
        url:`${value.url}?item=${encodeURIComponent(JSON.stringify(value.data))}`
      })
    }
  }
});
</script>

<style>

</style>
