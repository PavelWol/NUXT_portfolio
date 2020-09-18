<template>
  <header class="header">
    <img class="logo" src="~/assets/images/logo-straight.png" />
    <ul class="navigation">
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">about</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/references">references</nuxt-link>
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
  li
    list-style none
    padding-right 16px
    :last-child
      padding-right 0
    a
      font-size 16px
      text-decoration none
      color white
      text-transform uppercase
      font-family ITCAvantGardeProBold, sans-serif

</style>
