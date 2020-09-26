<template>
  <div class="wrapper">
    <AppHeader />
    <div class="mask">
      <Nuxt />
    </div>
    <Footer />
  </div>
</template>

<script>
  import AppHeader from '../components/AppHeader';
  import Footer from '../components/Footer';

  export default {
    components: {
      AppHeader,
      Footer
    },
    head: {
      bodyAttrs: {
        'class': 'body',
      }
    },
    mounted() {
      this.$nextTick(() => {
        this.$nuxt.$loading.start()

        setTimeout(() => this.$nuxt.$loading.finish(), 3000)
      })
    },
  };
</script>

<style lang="stylus">

*,*::before, *::after
  box-sizing border-box

body
  margin 0
  background: linear-gradient(90deg, rgba(15,25,39,1) 0,rgba(42,53,69,1) 100% );
  background-position center
  background-repeat no-repeat
  background-size cover
  overflow-x hidden

.wrapper
  width 100%
  max-width 1232px
  margin 0 auto
  padding 32px 24px 24px 24px
  position relative

/*.mask
  overflow hidden*/

h1, h2, h3, h4, h5, h6, p
  margin 0
  color white

a
  text-decoration none
  color white

.active-link.nuxt-link-exact-active
  color #df1a4a !important

.page-enter-active, .page-leave-active
  transition 500ms

.container.page-enter-active .main h1, .container.page-leave-active .main h1
  transition 500ms

.container.page-enter .main h1, .container.page-leave-to .main h1
  opacity 0
  transform translateY(15%)

.container.page-enter-active .main img, .container.page-leave-active .main img
  transition 500ms

.container.page-enter .main img, .container.page-leave-to .main img
  opacity 0
  transform translateY(-15%)

.page-enter, .page-leave-to
  opacity 0


</style>
