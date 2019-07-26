<template>
  <div class="menu-item" @click="toPage(itemUrl)">
      <div class="menu-content">
          <img class="menu-img" :src="itemIcon" background-size="cover"/>
          <p class="menu-p">{{itemName}}</p>
      </div>
  </div>
</template>

<script>
export default {
  props: ['itemName', 'itemIcon', 'itemUrl'],
  methods: {
    toPage (itemUrl) {
      const url = itemUrl
      if (mpvuePlatform === 'wx') {
        mpvue.navigateTo({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    }
  }
}
</script>

<style>
.menu-item {
  display: flex;
  margin-top: 20rpx;
}

.menu-content {
  width: 180rpx;
  height: 135rpx;
  align-items: center;
  border-width: 0 0 0 0;
  border-color: #E9E9E9;
  border-style: solid;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.menu-p {
  font-size: 15px;
  color: #111;
  padding-left: 5px;
  padding-top: 5px;
}

.menu-img {
  width: 85rpx;
  height: 78rpx;
}

</style>
