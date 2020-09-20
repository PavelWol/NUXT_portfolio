<template>
  <div v-if="loading" class="loading-page">
    <div class="loading"></div>
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
  padding-top 200px
  animation opacity 3s linear infinite

.loading
  width 160px
  height 160px
  border-radius 150px
  border 15px solid #fff
  border-top-color rgba(0,0,0,0.3)
  box-sizing border-box
  position absolute
  top 50%
  left 50%
  margin-top -80px
  margin-left -80px
  transition 500ms ease
  animation loading 1.2s linear infinite
  -webkit-animation loading 1.2s linear infinite

@keyframes loading
  0% transform rotate(0deg)

  100%
    transform rotate(360deg)
    -webkit-transform rotate(360deg)

@-webkit-keyframes loading
    0% -webkit-transform rotate(0deg)

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
