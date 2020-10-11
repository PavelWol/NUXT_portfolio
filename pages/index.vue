<template>
  <div class="container">
    <div class="main height-100 pt">

      <h1 data-glitch="WEBOVÝ KODER">
        webový
        <span>kodér</span>
      </h1>

      <div @click="openLaptop = !openLaptop" :class="{ open: openLaptop }" class="laptop js-laptop">
        <div class="laptop-top">
          <div class="laptop__lid"></div>
          <div class="laptop__screen">
            <video width="100%" height="100%" loop="true" autoplay="autoplay" muted>
              <source src="~/assets/images/timeline-mp.mp4" type="video/mp4">
              Your browser does not support the video tag.
            </video>
          </div>
        </div>
        <div class="laptop__base"></div>
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

  data() {
    return {
      openLaptop: false
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
};
</script>

<style scoped lang="stylus">

.main
  display flex
  align-items center

h1
  font-size 120px
  text-transform uppercase
  letter-spacing -6px
  text-align center
  span
    color #df1a4a

.imac
  width 50%


.laptop
  position absolute
  display flex
  flex-direction: column
  width 680px
  min-width 320px
  margin 0 16px
  cursor pointer

  .laptop-top
   height auto
   width 100%
   margin 0 auto
   perspective-origin 50% 100%
   perspective 2000px
   z-index 2


  .laptop__lid
    position absolute
    right 0
    bottom 0
    left 0
    margin 0 auto
    background: #e6e7e8
    height 10px
    width 100%
    border-radius 15px 15px 0 0
    border-bottom none
    transform rotateX(-90deg)
    transition all 10ms
    z-index 1
    perspective none


  .laptop__lid
    border-bottom 1px solid black
    transform rotateX(0)
    transition all 250ms
    transition-delay 150ms
  .laptop__screen
    transform rotateX(-90deg)


.open
  .laptop__screen
    transform rotateX(0)
  .laptop__lid
    transform rotateX(-90deg)
    transition all 100ms

.laptop__screen
  display flex
  justify-content center
  align-items center
  height 250px
  min-width 280px
  width calc(85% - 30px)
  margin 0 auto
  background-color #000
  border: 20px solid #373435
  border-right-width 15px
  border-left-width 15px
  border-radius: 15px 15px 0 0
  transform-origin center bottom
  transform rotateX(0deg)
  transform-style preserve-3d
  transition all 250ms ease-out
  &::before
    content ""
    position absolute
    top 0
    left 0
    width 100%
    height 100%
  &::after
    content: '';
    display: block;
    position: absolute;
    top: -12px;
    left: 50%;
    width: 1%;
    height: 1.5164%;
    margin-left: -0.5%;
    border-radius: 50%;
    background: #525252;

@media screen and (min-width: 600px)
  .laptop__screen
    height 350px

.laptop__base
  position relative
  background #e6e7e8
  width: 100%
  height 18px
  border-radius 0 0 15px 15px
  &::before
    content ""
    position absolute
    top 0
    left calc(50% - 75px)
    width 150px
    height 12px
    background-color #a9abae
    border-radius 0 0 15px 15px
    z-index 10
  &::after
    content ""
    position absolute
    right 0
    bottom -3px
    left 0
    width 95%
    margin 0 auto
    height 0
    box-shadow 0 0 10px 5px rgba(0, 0, 0, 0.5)
    border-radius 15px
    z-index -1



@media (max-width: 950px)

  .main
    flex-direction column
    .imac
      width 100%

  h1
    font-size 80px
    text-align center

</style>
