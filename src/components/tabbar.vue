<template>
  <div>
    <tabbar>
      <tabbar-item link="/lanyu">
        <img slot="icon" src="../assets/images/icon-1.png">
        <span slot="label">蓝雨</span>
      </tabbar-item>
      <tabbar-item :selected="selected" link="/">
        <img slot="icon" src="../assets/images/icon-2.png">
        <span slot="label">兴欣</span>
      </tabbar-item>
      <tabbar-item link="/lunhui">
        <img slot="icon" src="../assets/images/icon-3.png">
        <span slot="label">轮回</span>
      </tabbar-item>
      <tabbar-item link="/jiashi">
        <img slot="icon" src="../assets/images/icon-4.png">
        <span slot="label">嘉世</span>
      </tabbar-item>
    </tabbar>
  </div>
</template>

<script>
  import { Tabbar, TabbarItem } from 'vux'
  
  export default {
    components: {
      Tabbar,
      TabbarItem
    },
    data () {
      return {
        selected: true
      }
    }
  }
</script>
