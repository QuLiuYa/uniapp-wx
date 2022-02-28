<template>
  <view>
    <search @search-click="searchClick"></search>
    <u-tabs :list="list" :keyName="'value'" lineColor="#02d199" :activeStyle="{ color: '#02d199'}" itemStyle="height: 88rpx; padding-left: 48rpx; padding-right: 48rpx;" @change="change"></u-tabs>
    <div class="top-line"></div>
    <view class="list">
      <view class="list-item" v-for="(item, i) in 3" :key="i">
        <view class="list-item-head">
          <!-- 标题 -->
          <view class="title">
            <text class="title-tag">建议</text>
            <text class="title-name">市场监管总局：抽检发现5批次食品不合格存兽药残留等问题 </text>
          </view>
        </view>
        <view class="list-item-body">
          <!-- 内容 -->
          <view class="info">
            <view class="info-main">
              <!-- 发布人 -->
              <view class="author">
                <u--image :showLoading="true" shape="circle" src="https://cdn.uviewui.com/uview/album/1.jpg" width="40rpx" height="40rpx" errorIcon="../../static/images/logo.jpg"></u--image>
                <text class="author-name">皮皮皮</text>
              </view>
              <text class="desc">
                中央宣讲团成员，中共中央政治局委员、重庆市委书记陈敏尔在重庆作宣讲报告。他紧扣党的十九届四中全
              </text>
            </view>
            <view class="info-img">
              <image src="https://cdn.uviewui.com/uview/album/1.jpg" />
            </view>
          </view>
          <!-- 底部 -->
          <view class="footer">
            <text class="reply">0 回复</text>
            <text class="time">1 天前</text>
          </view>
        </view>
      </view>
    </view>
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
.list {
  background-color: #f4f6f8;
  .list-item {
    padding: 32rpx;
    margin-top: 24rpx;
    background-color: #fff;
    .title-tag {
      display: inline-block;
      width: 72rpx;
      height: 36rpx;
      // transform: scale(0.9);
      margin-right: 16rpx;
      line-height: 36rpx;
      text-align: center;
      background-color: #0166f8;
      border-radius: 18rpx 18rpx 18rpx 0rpx;
      font-size: 24rpx;
      color: #fff;
    }
    .title-name {
      line-height: 26rpx;
      font-size: 32rpx;
      font-weight: bold;
      color: #333;
    }
    &-body {
      .info {
        display: flex;
        margin: 28rpx 0 30rpx;
        &-main {
          flex: 1;
          .author {
            display: flex;
            align-items: center;
            margin-bottom: 15rpx;
            &-name {
              margin-left: 24rpx;
              line-height: 38rpx;
              font-size: 26rpx;
              color: #666;
            }
          }
          .desc {
            line-height: 40rpx;
            color: #333;
            display: -webkit-box;
            overflow: hidden;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
          }
        }
        &-img {
          width: 192rpx;
          height: 122rpx;
          image {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
    .footer {
      font-size: 26rpx;
      color: #999;
      .reply {
        display: inline-block;
        margin-right: 24rpx;
      }
    }
  }
}
</style>
