<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang="less">
@import '~vux/src/styles/reset.less';
html, body {
  height: 100%;
  width: 100%;
  overflow-x: hidden;
}

body {
  background-color: #fbf9fe;
}
.icon {
    width: 1.5em;
    height: 1.5em;
    vertical-align: -0.35em;
    fill: currentColor;
    overflow: hidden;
}
</style>
