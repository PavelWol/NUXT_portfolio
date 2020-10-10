<template>
  <div class="container">
    <div class="main height-100">

      <h1 data-glitch="WEBOVÝ KODER">
        webový
        <span>kodér</span>
      </h1>

      <div class="laptop-center">
        <div class="laptop"></div>
      </div>

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
  /*mounted() {
    var i = 0;
    var theLabel = document.getElementById("counter");

    this.$nextTick().then(() => {
      var interval = setInterval(() => {
        if (i === 100) clearInterval(interval);
        theLabel.innerHTML = i;
        i++;
      },
    100);
    })
  }*/
}
</script>

<style scoped lang="stylus">

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


.laptop-center
  position relative
  margin-left 80px


.laptop
  width 340px
  height 200px
  background #000
  border 16px solid #262626
  border-right-width 12px
  border-left-width 12px
  box-shadow 1px 0 0 #fff, -1px 0 0 #fff, 0 -1px 0 #fff
  overflow hidden
  &::before
    content ""
    position absolute
    bottom -10px
    left 50%
    transform translateX(-50%)
    width 130%
    height 10px
    background #fff
    border-top 2px solid #ccc
    border-bottom 4px solid #ccc
    border-top-left-radius 2px
    border-top-right-radius 2px
    border-bottom-left-radius 10px
    border-bottom-right-radius 10px
  &::after
    content ""
    position absolute
    width 4px
    height 4px
    border-radius 50%
    background #000
    left 50%
    top 6px


@media (max-width: 950px)

  .main
    flex-direction column
    .imac
      width 100%

  h1
    font-size 80px
    text-align center

</style>
