<template>
  <view>
    <search @search-click="searchClick"></search>
    <u-tabs :list="list" :keyName="'value'" lineColor="#02d199" :activeStyle="{ color: '#02d199'}" itemStyle="height: 88rpx; padding-left: 48rpx; padding-right: 48rpx;" @change="change"></u-tabs>
    <view class="bottom-line"></view>
  </view>
</template>

<script>
export default {
  data () {
    return {
      list: [
        {
          key: '',
          value: '首页'
        },
        {
          key: '1',
          value: '提问'
        },
        {
          key: '2',
          value: '建议'
        },
        {
          key: '3',
          value: '分享'
        },
        {
          key: '4',
          value: '讨论'
        },
        {
          key: '5',
          value: '公告'
        },
        {
          key: '6',
          value: '动态'
        }
      ]
    }
  },
  methods: {
    searchClick () {
      console.log(1111)
      uni.navigateTo({ url: '/packageA/search/search' })
    },
    change (item) {
      console.log(item, '----item----')
    }
  }
}
</script>

<style lang="scss">
</style>
