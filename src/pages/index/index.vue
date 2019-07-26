<template>
  <div class="main">
    <div class="main-banner">
      <img class="main-banner" src="/static/images/banner.png" background-size="cover" />
    </div>
    <div class="main-menu-1">
       <menuList v-bind:itemList="topItemList"></menuList>
    </div>
    <div class="main-space"></div>
    <panel :icon="compositePanelInfo.icon" :title="compositePanelInfo.title"></panel>
    <div class="main-menu-2">
           <menuList v-bind:itemList="compositeItemList"></menuList>
    </div>
    <div class="main-space"></div>
    <panel :icon="inpatientPanelInfo.icon" :title="inpatientPanelInfo.title"></panel>
    <div class="main-menu-2">
      <menuList v-bind:itemList="compositeItemList"></menuList>
    </div>
    <div class="main-space"></div>
    <panel :icon="inpatientPanelInfo.icon" :title="inpatientPanelInfo.title"></panel>
    <div class="main-menu-2">
      <menuList v-bind:itemList="compositeItemList"></menuList>
    </div>
  </div>
</template>

<script>
import menuList from '@/components/menuList'
import panel from '@/components/panel'

export default {
  data () {
    return {
      topItemList: [
        {
          itemName: '挂号',
          itemIcon: '/static/images/icon-guahao.png',
          itemUrl: './pages/counter/main'
        },
        {
          itemName: '门诊缴费',
          itemIcon: '/static/images/icon-jiaofei.png',
          itemUrl: './pages/counter/main'
        },
        {
          itemName: '报告查询',
          itemIcon: '/static/images/icon-baogao.png',
          itemUrl: '../pages/counter/main'
        },
        {
          itemName: '排队就诊',
          itemIcon: '/static/images/icon-paidui.png',
          itemUrl: '../../pages/counter/main'
        }
      ],
      compositeItemList: [
        {
          itemName: '挂号记录',
          itemIcon: '/static/images/icon-guahaojilu.png',
          itemUrl: './pages/counter/main'
        },
        {
          itemName: '缴费记录',
          itemIcon: '/static/images/icon-jiaofeijilu.png',
          itemUrl: './pages/counter/main'
        },
        {
          itemName: '电子处方',
          itemIcon: '/static/images/icon-chufang.png',
          itemUrl: '../pages/counter/main'
        },
        {
          itemName: '满意度调查',
          itemIcon: '/static/images/icon-manyidu.png',
          itemUrl: '../../pages/counter/main'
        },
        {
          itemName: '来院导航',
          itemIcon: '/static/images/icon-laiyuan.png',
          itemUrl: './pages/counter/main'
        },
        {
          itemName: '院内导航',
          itemIcon: '/static/images/icon-yuannei.png',
          itemUrl: './pages/counter/main'
        },
        {
          itemName: '名医名科',
          itemIcon: '/static/images/icon-mingyimingke.png',
          itemUrl: '../pages/counter/main'
        },
        {
          itemName: '长沙名医',
          itemIcon: '/static/images/icon-changshamingyi.png',
          itemUrl: '../../pages/counter/main'
        }
      ],
      compositePanelInfo: {
        icon: '/static/images/icon-title.png',
        title: '综合服务'
      },
      inpatientPanelInfo: {
        icon: '/static/images/icon-inpatient-title.png',
        title: '住院服务'
      }
    }
  },
  components: {
    menuList, panel
  },
  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.main-banner {
  width: 100%;
  height: 182rpx;
}

.main-space {
  margin-top: 25rpx;
  width: 99.5%;
  height: 20rpx;
  background: #D9D9D9;
}

.main-menu-1 {
  margin: 20rpx 0 20rpx 0;
}

.main-menu-2 {
  margin: 20rpx 0 20rpx 0
}
</style>
