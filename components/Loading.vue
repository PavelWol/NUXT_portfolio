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
  animation opacity 6s ease


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
    content "VÍTEJTE"
    font-size 120px
    color white
    font-family ITCAvantGardeProBold, sans-serif
    animation textChange 6s linear
    position relative
    z-index 0
  &::before
    content ""
    background #df1a4a
    height 0
    width 100%
    max-width 90%
    position absolute
    z-index 1
    bottom 0
    transition 1s ease
    animation bg 2s linear
    animation-delay 2s


@keyframes bg
	0%
    height 0
    top 50%
    transform translateY(-50%)

  40%
    height 25%

	100%
    height 0
    transform translateY(-50%)
    top 50%


@keyframes textChange
	0%
		content "WEBOVÝ KODÉR"

	40%
		content "WEBOVÝ KODÉR"

	60%
		content "VÍTEJTE"

  80%
    transform translateX(0)

  90%
    transform translateX(-300%)

	99%
		content "VÍTEJTE"

  100%
    transform translateX(-300%)



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

@media (max-width: 1100px)

  .background
    &::after
      font-size 80px


@media (max-width: 950px)

  .background
    &::before
      width calc(100% - 48px)
    &::after
      font-size 38px

</style>
