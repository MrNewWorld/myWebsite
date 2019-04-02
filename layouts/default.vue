<template>
  <div class="flex flex-column h-100">
    <div class="bg">
      <video src="../assets/common/galaxy2.mp4" muted loop autoplay />
    </div>
    <AppHeader />
    <transition name="slide-fade">
      <div v-show="show" class="flex flex-auto w-90 center bg-black-50 ph5-ns justify-center items-center self-center">
        <Nuxt />
      </div>
    </transition>
    <Footer />
  </div>
</template>

<script>
import AppHeader from './header'
import Footer from './footer'

export default {
  components: {
    Footer,
    AppHeader
  },
  data() {
    return {
      show: false
    }
  },
  created() {
    // setInterval(() => {
    //   this.show = !this.show
    // }, 2000)
  },
  mounted() {
    this.show = true
    this.$root.$on('go', () => {
      this.show = false
      if (!this.show) {
        this.show = true
      }
    })
  }
}
</script>

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
body, html {
  height: 100%;
  overflow: hidden;
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

.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to {
  transform: translateX(100%);
  opacity: 0;
}
</style>
