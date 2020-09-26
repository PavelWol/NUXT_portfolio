<template>
  <div class="container">
    <div class="main height-100">

      <h1 data-glitch="WEBOVÝ KODER">
        webový
        <span>kodér</span>
      </h1>
      <transition name="animate">
        <img v-show="show" class="imac" src="~/assets/images/imac.png" alt="" />
      </transition>
      <div @click="show = !show">click me</div>

    </div>
  </div>
</template>

<script>
export default {
  head() {
      return {
        title: 'Pavel Wolinger | Webový kodér',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'about me page'
          }
        ]
      }
    },
  data () {
    return {
      show: false
    }
  }
  }
</script>

<style scoped lang="stylus">

.animate-enter-active, .animate-leave-active
  transition 500ms ease

.animate-enter, .animate-leave-to
  opacity 0

.animate-enter-to, .animate-leave
  opacity 1

.main
  display flex
  align-items center

h1
  font-size 120px
  text-transform uppercase
  letter-spacing -6px
  text-align right
  span
    color #df1a4a

.imac
  width 50%

</style>
