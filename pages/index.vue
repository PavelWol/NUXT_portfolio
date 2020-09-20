<template>
  <div class="container pt">
    <div class="main height-100">

      <h1>
        webový
        <span>kodér</span>
      </h1>
      <img class="imac" src="~/assets/images/imac.png" alt="" />

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

h1
  font-size 120px
  font-family ITCAvantGardeProBold
  text-transform uppercase
  letter-spacing -6px
  text-align right
  span
    color #df1a4a

.imac
  width 50%

</style>
