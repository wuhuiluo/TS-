<template>
  <div id="app">
    <transition>
      <router-view />
    </transition>
  </div>
</template>
<script>
export default {
  mounted() {
    setTimeout(() => {
      window.L2Dwidget.init({
        pluginRootPath: "live2dw/",
        pluginJsPath: "lib/",
        pluginModelPath: "live2d-widget-model-z16/assets/",
        tagMode: false,
        debug: false,
        model: {
          jsonPath: "../live2dw/live2d-widget-model-z16/assets/z16.model.json"
        },
        display: { position: "left", width: 300, height: 400 },
        mobile: { show: true },
        log: false
      });
    }, 1000);
  }
};
</script>
<style lang="less">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
</style>
