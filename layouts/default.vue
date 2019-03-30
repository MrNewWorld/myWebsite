<template>
  <div class="h-100">
    <div class="bg">
      <video src="../assets/common/galaxy.mp4" muted loop autoplay />
    </div>
    <Nuxt class="flex flex-column h-100" />
  </div>
</template>

<style lang="less">
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  height: 100%;
}
body {
  height: 100%;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
#__layout, #__nuxt {
  height: 100%;
}
.bg {
  position: fixed;
  width: 100vw;
  height: 100%;
  z-index: -1;
  video {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
</style>
