<template>
  <nav class="nav dt w-100 border-box pa4 pa5-ns">
    <div class="dtc v-mid w-90 tr">
      <nuxt-link to="/" class="link dim white f4 f3-ns dib mr3 mr6-ns mr5-m" title="首页">
        首页
      </nuxt-link>
      <nuxt-link to="/blog" class="link dim white f4 f3-ns dib mr3 mr6-ns mr5-m" title="文章">
        文章
      </nuxt-link>
      <nuxt-link to="/project" class="link dim white f4 f3-ns dib mr3 mr6-ns mr5-m" title="作品">
        作品
      </nuxt-link>
      <nuxt-link to="/about" class="link dim white f4 f3-ns dib mr3 mr6-ns mr5-m" title="关于">
        关于
      </nuxt-link>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="less" scoped>
  .nav{
    flex: 0 1 auto;
  }
</style>
