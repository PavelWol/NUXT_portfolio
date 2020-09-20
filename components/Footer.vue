<template>
  <div class="socials">
    <div class="online-text">
      <p>
        Najdete mně online nebo <nuxt-link to="/contact">mi napište</nuxt-link>.
      </p>
    </div>
    <div class="sm-links">
      <a href="mailto:pw.wolinger@gmail.com">
        <img src="~/assets/images/email.png" alt="">
        <p>pw.wolinger@gmail.com</p>
      </a>
      <div class="spacer-lg"></div>
      <a href="tel:+420 777 051 053">
        <img src="~/assets/images/phone.png" alt="">
        <p>+420 777 051 053</p>
      </a>
      <div class="spacer-lg"></div>
      <a href="">
        <img src="~/assets/images/facebook.png" alt="">
        <p>Facebook</p>
      </a>
      <div class="spacer-lg"></div>
      <a href="">
        <img src="~/assets/images/github.png" alt="">
        <p>Github</p>
      </a>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Footer'
}

</script>

<style scoped lang="stylus">

.online-text
  border-top 1px solid white
  padding-top 32px
  padding-bottom 16px
  max-width 35%
  width 100%
  p
    font-size 18px
    a
      blue

.sm-links
  width 100%
  padding-bottom 40px
  display flex
  justify-content space-between

  a
    display flex
    align-items center
    text-decoration none

  p
    font-size 16px
    letter-spacing -1.13px

  img
    width 24px
    margin-right 24px

</style>
