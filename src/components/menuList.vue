<template>
  <div class="menu-list">
      <div v-for="(item,index) in itemList" :key="index">
          <menuItem :itemName="item.itemName" :itemIcon="item.itemIcon" :itemUrl="item.itemUrl"></menuItem>
      </div>
  </div>
</template>

<script>
import menuItem from '@/components/menuItem'
export default {
  props: {
    itemList: {
      type: Array,
      default: () => []
    }
  },
  components: {
    menuItem
  }
}
</script>

<style>
.menu-list {
  display: flex;
  flex-direction: row;
  flex-wrap:wrap;
}
</style>
