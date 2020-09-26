<template>
  <header class="header">
    <nuxt-link to="/">
      <img class="logo" src="~/assets/images/logo-straight.png" alt="" />
    </nuxt-link>
    <ul class="navigation">
      <li>
        <nuxt-link class="active-link" to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link class="active-link" to="/about">o mně</nuxt-link>
      </li>
      <li>
        <nuxt-link class="active-link" to="/references">reference</nuxt-link>
      </li>
      <li>
        <nuxt-link class="active-link" to="/contact">kontakt</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<script>

  export default {
    name: 'AppHeader'
  }

</script>

<style scoped lang="stylus">

.header
  display flex
  justify-content space-between

.logo
  height 30px

.navigation
  padding 0
  margin 0
  display flex
  align-items center
  > :first-child
    border-right 1px solid white
  > :nth-child(2)
    padding-left 16px
  li
    list-style none
    padding-right 16px
    &:last-child
      padding-right 0
    &:hover
      color #df1a4a
    a
      font-size 16px
      text-decoration none
      color white
      font-weight bold
      text-transform uppercase
      font-family ITCAvantGardeProBold, sans-serif
      transition 250ms ease

@media (max-width: 950px)

  .navigation
    position fixed
    justify-content space-between
    max-width calc(450px - 48px)
    transform translateX(-24px)
    bottom 0
    width 100%
    z-index 99
    background-color #c1cedc
    padding 16px

</style>
