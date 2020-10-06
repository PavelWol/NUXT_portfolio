<template>
  <div class="container">
    <div class="main height-100">

      <h1 data-glitch="WEBOVÝ KODER">
        webový
        <span>kodér</span>
      </h1>
      <!--<div style="color: white;" id="counter"></div>-->
      <img class="imac" src="~/assets/images/imac.png" alt="" />

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

@media (max-width: 950px)

  .main
    flex-direction column
    .imac
      width 100%

  h1
    font-size 80px
    text-align center

</style>
