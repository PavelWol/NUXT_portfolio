<template>
  <div class="container">
    <div class="main">

      <h1>
        webovy koder
      </h1>
      <img class="imac" src="~/assets/images/imac.png" />

    </div>
  </div>
</template>

<script>
export default {
  head() {
      return {
        title: 'Welcome',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'about me page'
          }
        ]
      }
    }
}
</script>

<style scoped lang="stylus">

.main
  display flex
  align-items center
  position absolute
  top 50%
  transform translateY(-50%)

h1
  font-size 120px
  font-family ITCAvantGardeProBold, sans-serif
  text-transform uppercase
  letter-spacing -6px
  text-align right

.imac
  width 50%

</style>
