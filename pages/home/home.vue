<template>
  <view>
    <search @search-click="searchClick"></search>
    <view class="bottom-line"></view>
  </view>
</template>

<script>
export default {
  data () {
    return {
    }
  },
  methods: {
    searchClick () {
      console.log(1111)
      uni.navigateTo({ url: '/packageA/search/search' })
    }
  }
}
</script>

<style lang="scss">
</style>
