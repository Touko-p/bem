<template>
  <all-page :show-bar="values.showBar">
    <introduce>
      <block v-if="values.value1&&!values.value2">
        <block v-for="(v,k) in values.value1" :key="k">
          <item :title="v.title" :phone="v.phone"></item>
        </block>
      </block>
      <block v-if="values.value2&&values.value1">
        <block v-for="(v,k1) in values.value1" :key="k1">
          <item :title="v.title">
            <block v-for="(v,k2) in values.value2" :key="k2">
              <info :title="v"></info>
            </block>
          </item>
        </block>
      </block>
    </introduce>
    <bar v-if="values.showBar"></bar>
  </all-page>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator';
import allPage from "@/components/allPage/index.vue";
import introduce from '@/components/introduce/index.vue';
import item from "@/components/item/index.vue";
import info from "@/components/info/index.vue";
import bar from "@/components/bar/index.vue";

@Component({
  components: {
    allPage, introduce, item, info, bar
  }
})

export default class Index extends Vue {
  values = null

  onLoad(option: any) {
    const item = JSON.parse(decodeURIComponent(option.item));
    this.values = item
  }
}
</script>

<style scoped>

</style>