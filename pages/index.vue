<template>
  <div class="container">
    <div>

      <h1 class="title">
        portfolio
      </h1>
      <img class="imac" src="~/assets/images/imac.png" />

    </div>
  </div>
</template>

<script>
export default {
  head() {
      return {
        title: 'Welcome',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'about me page'
          }
        ]
      }
    }
}
</script>

<style lang="stylus">

.imac
  width 500px

</style>
