<script>
export default {
  onLaunch: function () {
    console.log('App Launch')
  },
  onShow: function () {
    console.log('App Show')
  },
  onHide: function () {
    console.log('App Hide')
  }
}
</script>

<style lang="scss">
@import '@/uni_modules/uview-ui/index.scss';
.top-line {
  height: 5rpx;
  background: transparent;
  box-shadow: 0 4rpx 6rpx rgba(0, 0, 0, 0.05);
}
.bottom-line {
  position: fixed;
  bottom: -5rpx;
  left: 0;
  width: 100vw;
  height: 5rpx;
  background: transparent;
  box-shadow: 0 -5rpx 5rpx rgba(0, 0, 0, 0.05);
}
</style>
