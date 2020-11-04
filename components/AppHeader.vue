<template>
  <header class="header">
    <nuxt-link class="logo-block" to="/">
      <img class="logo" src="~/assets/images/logo-straight.png" alt="" />
    </nuxt-link>
    <nav style="display: none;" :class="{ mobileNav: navActive }">
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
    <div style="display: none;" @click="navActive = !navActive" :class="{ cross: navActive }" class="openMenu">
      <div style="height: 25px;" @click="bodyOverflow">
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
        navActive: false
      }
    },
    methods: {
      bodyOverflow() {
        document.querySelector(".body").classList.toggle("overflow");
      }
    },
    watch: {
    '$route' () {
      this.navActive = false
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
    background linear-gradient(90deg, #0f1927 0, #2a3545 100%)

  .openMenu
    position absolute
    z-index 10
    top 5px
    right 5px
    width 30px
    height 25px
    cursor pointer
    span
      position absolute
      display block
      width 35px
      background white
      height 2px
      transition 250ms ease
      &:first-child
        top 0
      &:nth-child(2)
        top 10px
      &:last-child
        top 20px
  &.cross
    span
      transition 250ms ease
      &:first-child
        transform-origin 0 100%
        transform rotate(45deg) translate(-4px)
      &:nth-child(2)
        width 0
      &:last-child
        transform-origin 0 0
        transform rotate(-45deg) translate(-4px)


  .mobileNav .navigation
    display block
    li
      padding 16px
      border none
      text-align center
      opacity 0
      animation navList .5s linear
      animation-fill-mode: forwards;
      &:nth-child(2)
        animation-delay .2s
      &:nth-child(3)
        animation-delay .3s
      &:nth-child(4)
        animation-delay .4s
      a
        font-size 24px

@keyframes navList

  0%
    transform translateX(25%)
    opacity 0

  100%
    transform translateX(0)
    opacity 1

@media (min-width: 950px)

  .openMenu
    display none


</style>
