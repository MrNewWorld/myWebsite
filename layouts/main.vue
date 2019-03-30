<template>
  <section class="flex flex-auto w-90 center bg-black-50 ph5-ns justify-center items-center self-center">
    <slot />
  </section>
</template>

<script>
export default {
  name: 'Main'
}
</script>

<style lang="less" scoped>
.main{
  width: 100vw;
  height: 100%;
  background-color: rgba(0,0,0,.5);
}
</style>
