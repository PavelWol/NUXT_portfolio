<template>
  <div class="socials">
    <div class="online-text">
      <p>
        Najdete mně online nebo <nuxt-link to="/contact">mi napište</nuxt-link>.
      </p>
    </div>
    <div class="copyright">
      <p>
        Pavel Wolinger © Copyright 2020. All Rights Reversed.
      </p>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Footer'
}

</script>

<style scoped lang="stylus">

.socials
  margin-top 120px

.online-text
  border-top 1px solid white
  padding-top 32px
  padding-bottom 48px
  max-width 35%
  width 100%
  p
    font-size 18px
    a
      color #df1a4a
      transition 250ms ease
      &:hover
        border-bottom 1px solid #df1a4a
        transition 250ms ease

.copyright
  width 100%
  padding-bottom 40px
  display flex
  justify-content center

  a
    display flex
    align-items center
    text-decoration none

  p
    font-size 16px
    letter-spacing -1.13px
    color rgba(255, 255, 255, .5)

  img
    width 24px
    margin-right 24px

@media (max-width: 950px)

  .online-text
    max-width unset


  .copyright
    padding-bottom 80px

</style>
