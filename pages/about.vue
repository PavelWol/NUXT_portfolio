<template>
  <div class="pt about-me">
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
          žádná výzva. Co neznám to se naučím, svou práci miluji a baví mě
          učit se novým věcem
        </p>
        <div class="spacer-lg"></div>
        <div class="spacer-lg"></div>
        <div class="rectanglephoto">
          <!--<img src="img/icons/rectanglephoto.svg" alt="">-->
        </div>
        <div class="chart">
          <!--<img src="img/bg/chart.png" alt="" />-->
        </div>
      </article>
    </div>
  </div>
</template>

<script>
  export default {
    head() {
      return {
        title: 'about me',
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

<style scoped lang="stylus">

.about-me
  display flex
  max-width 1232px
  width 100%
  margin 0 auto


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
  font-size 32px
  line-height 1.69
  letter-spacing -0.67px
  color #c1cedc


.chart img
  width 75%


</style>
