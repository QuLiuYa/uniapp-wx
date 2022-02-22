<template>
  <view class="search">
    <view class="search-box" :style="{ 'padding-top': barHeight + 'px' }">
      <u-search placeholder="搜索社区内容" shape="round" :disabled="true" :showAction="false" @click="$emit('search-click')"></u-search>
    </view>
  </view>
</template>

<script>
export default {
  data () {
    return {
      barHeight: 0
    }
  },
  beforeMount () {
    this.getBarHeight()
  },
  methods: {
    getBarHeight () {
      try {
        const res = uni.getSystemInfoSync()
        const isIOS = res.system.indexOf('iOS') > -1
        if (isIOS) {
          this.barHeight = res.statusBarHeight + 4
        } else {
          this.barHeight = res.statusBarHeight + 7
        }
      } catch (e) {
        // error
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.search {
  padding: 0 32rpx 12rpx;
  &-box {
    width: 60%;
    @media screen and(max-width: 320px) {
      width: 50%;
    }
  }
}
</style>
