<template>
    <div class="panel">
      <div class="panel-title"><img class="panel-img" :src="icon" background-size="cover"/><span class="panel-span">{{title}}</span></div>
    </div>
</template>

<script>
  export default {
    props: ['icon', 'title']
  }
</script>

<style scoped>
  .panel {
    display: flex;
    width: 100%;
    margin-top: 10rpx;
    margin-left: 10prx;
  }
  .panel-title {
    display: flex;
    padding-left: 20rpx;
  }
  .panel-img {
    width: 44rpx;
    height: 54rpx;
  }

  .panel-span {
    margin-left: 10rpx;
    font-size: 38rpx;
    font-weight: bold;
    color: cornflowerblue;
  }
</style>
