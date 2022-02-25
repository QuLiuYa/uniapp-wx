<template>
  <view>
    <view class="search-box">
      <u-search placeholder="请输入搜索内容" v-model="keyword"></u-search>
    </view>
    <view class="history" v-if="historyList.length">
      <view class="history-title">
        <text>搜索历史</text>
        <u-icon name="trash" size="28"></u-icon>
      </view>
      <view class="history-wrap">
        <u-tag v-for="(item, i) in historyList" :key="i" :text="item" type="info" borderColor="#fff" shape="circle" plain plainFill></u-tag>
      </view>
    </view>
    <div class="hot">
      <view class="hot-title">热门搜索</view>
      <view class="hot-wrap">
        <u-tag v-for="(item, i) in hotList" :key="i" :text="item" type="info" borderColor="#fff" shape="circle" plain plainFill></u-tag>
      </view>
    </div>
  </view>
</template>

<script>
export default {
  data () {
    return {
      keyword: '',
      historyList: ['前端', '后端', 'Java', 'javaScript', '小程序', '算法'],
      hotList: ['前端', '后端', 'Java', 'javaScript', '小程序', '算法']
    }
  }
}
</script>

<style lang="scss" scoped>
.search-box {
  padding: 24rpx;
}
.history,
.hot {
  padding: 24rpx;
  margin-bottom: 30rpx;
  &-title {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20rpx;
  }
  &-wrap {
    display: flex;
    flex-wrap: wrap;
    /deep/ .u-tag-wrapper {
      margin: 20rpx 20rpx 0 0;
    }
  }
}
</style>
