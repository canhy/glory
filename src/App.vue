<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
import Common from './components/'
export default {
  name: 'app',
  components: Common
}
</script>

<style lang="less">
@import '~vux/src/styles/reset.less';

html, body {
  background-color: #fbf9fe;
  height: 100%;
}
#app {
  height: 100%;
}
</style>
