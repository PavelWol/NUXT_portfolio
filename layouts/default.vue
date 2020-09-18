<template>
  <div class="wrapper">
    <AppHeader />
    <Nuxt />
  </div>
</template>

<script>
  import AppHeader from '../components/AppHeader';

  export default {
    components: {
      AppHeader
    },
    head: {
      bodyAttrs: {
        'class': 'body',
      }
    },
  };
</script>

<style lang="stylus">

@font-face
  font-family ITCAvantGardeProBold
  src local('AvantBold') url(../assets/fonts/ITCAvantGardeProBold.otf)

@font-face
  font-family ITCAvantGardeProBk
  src local('AvantBk') url(../assets/fonts/ITCAvantGardeProBk.otf)

@font-face
  font-family ITCAvantGardeProMd
  src local('AvantMd') url(../assets/fonts/ITCAvantGardeProMd.otf)

*,*::before, *::after
  box-sizing border-box

body
  margin 0
  background: linear-gradient(90deg, rgba(15,25,39,1) 0,rgba(42,53,69,1) 100% );
  background-position center
  background-repeat no-repeat
  background-size cover
  overflow-x hidden
  height 100vh

.wrapper
  width 100%
  max-width 1232px
  margin 0 auto
  padding 24px
  height 100vh
  position relative

h1, h2, h3, h4, h5, h6
  margin 0
  color white

.page-enter-active, .page-leave-active
  transition all 500ms ease

.page-enter, .page-leave-active
  opacity 0

</style>
