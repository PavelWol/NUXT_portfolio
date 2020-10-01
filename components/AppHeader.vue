<template>
  <header class="header">
    <nuxt-link class="logo-block" to="/">
      <img class="logo" src="~/assets/images/logo-straight.png" alt="" />
    </nuxt-link>
    <nav :class="{ mobileNav: show }">
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
    </nav>
    <div @click="show = !show" :class="{ cross: show }" class="openMenu">
      <div style="height:  25px;" @click="bodyClass">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
  </header>
</template>

<script>

  export default {
    name: 'AppHeader',
    data() {
      return {
        show: false
      }
    },
    methods: {
      bodyClass() {
        document.querySelector(".body").classList.toggle("hovno");
      }
    }
  }

</script>

<style scoped lang="stylus">

.header
  display flex
  justify-content space-between
  position relative

.logo-block
  position relative
  z-index 11

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
    display none

  .mobileNav
    position fixed
    z-index 10
    top 50%
    left 50%
    transform translate(-50%, -50%)
    height 100vh
    width 100%
    display flex
    justify-content center
    align-items center
    background-color black

  .openMenu
    position absolute
    z-index 10
    top 0
    right 0
    width 30px
    height 25px
    cursor pointer
    span
      position absolute
      display block
      width 30px
      background white
      height 2px
      &:first-child
        top 0
      &:nth-child(2)
        top 10px
      &:last-child
        top 20px


  .mobileNav .navigation
    display block


@media (min-width: 950px)

  .openMenu
    display none


</style>
