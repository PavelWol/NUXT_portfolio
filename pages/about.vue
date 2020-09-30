<template>
  <div class="pt about-me">
    <h2 data-glitch="TOHLE JSEM JÁ">
      TOHLE JSEM
      <span>JÁ</span>
    </h2>
    <div class="height-100">
      <div class="container">
        <div class="photo">
          <img src="~/assets/images/picme.png" alt="">
        </div>
        <div class="scene-2">
          <div class="rectanglephoto4">
            <!--<img src="img/icons/rectanglephoto4.svg" alt="">-->
          </div>
          <div class="dotsphoto1">
            <!--<img src="img/bg/dotsphoto1.png" alt="">-->
          </div>
          <div class="rectanglephoto2">
            <!--<img src="img/icons/rectanglephoto2.svg" alt="">-->
          </div>
          <div class="rectanglephoto3">
            <!--<img src="img/icons/rectanglephoto3.svg" alt="">-->
          </div>
          <div class="ovalphoto">
            <!--<img src="img/icons/ovalphoto.svg" alt="">-->
          </div>
        </div>
      </div>
      <article class="about-chart">
        <h4>Pár slov o mně</h4>
        <div class="spacer-lg"></div>
        <p>
          Jmenuji se Pavel Wolinger a jsem nadšený kodér, kterého neodradí
          žádná výzva. S kodéřinou jsem začal poměrně nedávno,
          proto v tuto chvíli prohlubuji své znalosti a dovednosti,
          abych mohl v blízké budoucnosti pracovat na tvorbě zajímavých webů a webových aplikací.
        </p>
        <div class="spacer-lg"></div>
        <div class="rectanglephoto">
          <!--<img src="img/icons/rectanglephoto.svg" alt="">-->
        </div>
        <div class="animated-skills first">
          <div class="first-skill"></div>
          <span>HTML</span>
        </div>
        <div class="animated-skills second">
          <div class="second-skill"></div>
          <span>CSS</span>
        </div>
        <div class="animated-skills third">
          <div class="third-skill"></div>
          <span>JAVASCRIPT</span>
        </div>
      </article>
    </div>
  </div>
</template>

<script>
  export default {
    head() {
      return {
        title: 'O mně',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'o mne'
          }
        ]
      }
    }
  }

</script>

<style scoped lang="stylus">

.animated-skills
  width 100%
  height 18px
  margin-top 32px
  display flex
  position relative
  max-width 450px
  .first-skill
    height 18px
    background-color #df1a4a
    animation progress 5s forwards
    animation-iteration-count 1
    &:after
      content " "
      position absolute
      display block
      width 100%
      height 100%
      top 0
      left 0
      z-index -1
      background #df1a4a
      transform-origin bottom left
      -ms-transform skew(-30deg, 0deg)
      -webkit-transform skew(-30deg, 0deg)
      transform skew(-30deg, 0deg)
      animation progress 5s forwards
  span
    font-size 16px
    position absolute
    right -48px
    transform translateX(100%)
    color #df1a4a
    font-family ITCAvantGardeProBold, sans-serif
.second
  max-width 350px
  .second-skill
    background-color #34b4eb
    animation progress 5s forwards
    animation-iteration-count 1
    &:after
      content " "
      position absolute
      display block
      width 100%
      height 100%
      top 0
      left 0
      z-index -1
      background #34b4eb
      transform-origin bottom left
      -ms-transform skew(-30deg, 0deg)
      -webkit-transform skew(-30deg, 0deg)
      transform skew(-30deg, 0deg)
      animation progress 5s forwards
  span
    color #34b4eb
.third
  max-width 250px
  .third-skill
    background-color #34ebdc
    animation progress 5s forwards
    animation-iteration-count 1
    &:after
      content " "
      position absolute
      display block
      width 100%
      height 100%
      top 0
      left 0
      z-index -1
      background #34ebdc
      transform-origin bottom left
      -ms-transform skew(-30deg, 0deg)
      -webkit-transform skew(-30deg, 0deg)
      transform skew(-30deg, 0deg)
      animation progress 5s forwards
  span
    color #34ebdc

@keyframes progress
  from
    width 0

  to
    width 100%

.about-me
  min-height calc(100vh - 54px)

.about-me .height-100
  min-height unset
  padding-top 5%

.container
  position relative


.scene-2
  position absolute
  width 100%
  height 100%
  top 0


.photo
  padding-right 10%
  width 80%


.photo img
  width 100%
  box-shadow 0 30px 133px -12px rgba(0,0,0,1)
  border-radius 50%


.rectanglephoto
  position absolute
  bottom 150px
  right 70px


.rectanglephoto img
  animation sink 4s ease-in-out infinite


.rectanglephoto2
  position absolute
  z-index 1
  bottom 200px
  left 55px


.rectanglephoto2
  animation sink 4s ease-in-out infinite


.rectanglephoto3
  position absolute
  right 70px
  bottom 200px


.rectanglephoto3
  animation left 4s ease-in-out infinite


.rectanglephoto4
  position absolute
  z-index 2
  left 35%
  top -50px


.rectanglephoto4 img
  animation sink 4s ease-in-out infinite


.dotsphoto1
  position absolute
  width 65%
  bottom 80px
  left 5px


.dotsphoto1 img
  width 100%
  animation sink 6s ease-in-out infinite


.ovalphoto
  position absolute
  bottom 0
  left 150px


.ovalphoto
  animation rotate 6s ease-in-out infinite



.about-chart
  display flex
  flex-direction column
  justify-content space-between
  position relative
  max-width 768px
  width 100%


.about-chart p
  font-size 28px
  line-height 1.69
  letter-spacing -0.67px
  color #c1cedc


.chart img
  width 75%

@media (max-width: 950px)

  .about-me .height-100
    flex-direction column

  .photo
    margin 32px auto
    padding 0

  .about-chart
    p
      font-size 24px

  .animated-skills span
    transform unset
    top -22px
    right unset

  .first
    max-width 300px

  .second
    max-width 250px

  .third
    max-width 200px

</style>
