<template>
  <div v-if="loading" class="loading-page">
    <div class="background"></div>
  </div>
</template>

<script>
export default {
  data: () => ({
    loading: false
  }),
  methods: {
    start () {
      this.loading = true
    },
    finish () {
      this.loading = false
    }
  }
};
</script>

<style scoped lang="stylus">

.loading-page
  position fixed
  z-index 999
  top 0
  left 0
  width 100%
  height 100%
  background rgba(0, 0, 0, 1)
  text-align center
  display flex
  justify-content center
  align-items center
  animation opacity 8s linear


.background
  width 100%
  height 100vh
  background linear-gradient(90deg, #0f1927 0, #2a3545 100%)
  position relative
  transition 1s ease
  display flex
  justify-content center
  align-items center
  &::after
    content "VÍTEJTE NA MÉM PORTFOLIU"
    font-size 120px
    color white
    font-family ITCAvantGardeProBold, sans-serif
    animation textChange 6s linear
  &::before
    content ""
    background #df1a4a
    height 0
    width 100%
    position absolute
    bottom 0
    transition 1s ease
    animation bg 3s linear
    animation-delay 1.5s


@keyframes bg
	0%
		height 0
		top 0

	40%
		height 100%

	50%
		height 100%

  60%
    height 100%

	100%
		height 0
		bottom 0
		top unset


@keyframes textChange
	0%
		content "WEBOVÝ KODÉR"

	40%
		content "WEBOVÝ KODÉR"

	60%
		content "VÍTEJTE NA MÉM PORTFOLIU"

	100%
		content "VÍTEJTE NA MÉM PORTFOLIU"



@keyframes opacity
  0%
    opacity 1
  50%
    opacity 1
  75%
    opacity 1
  90%
    opacity 1
  100%
    opacity 0

</style>
