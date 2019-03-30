<template>
  <section>
    <AppHeader />
    <Main>
      <slot />
    </Main>
    <Footer />
  </section>
</template>

<script>
import AppHeader from './header'
import Main from './main'
import Footer from './footer'

export default {
  components: {
    Footer,
    AppHeader,
    Main
  }
}
</script>
