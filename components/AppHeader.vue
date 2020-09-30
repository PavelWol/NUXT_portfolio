<template>
  <header class="header">
    <nuxt-link to="/">
      <img class="logo" src="~/assets/images/logo-straight.png" alt="" />
    </nuxt-link>
    <ul class="navigation">
      <li v-for="item in navItems">
        <nuxt-link :to=item.link class="active-link">{{item.text}}</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<script>

  export default {
    name: 'AppHeader',
    data() {
      return {
        navItems: [
          {
            text: 'Home',
            link: '/'
          },
          {
            text: 'About',
             link: '/about'
          },
          {
            text: 'References',
            link: '/references'
          },
          {
            text: 'Contact',
            link: '/contact'
          },
        ]
      }
    },
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
    :last-child
      padding-right 0
    :hover
      color #df1a4a
    a
      font-size 16px
      text-decoration none
      color white
      font-weight bold
      text-transform uppercase
      font-family ITCAvantGardeProBold, sans-serif
      transition 250ms ease

</style>
