<template>
  <div class="">
    <div class="references">
      <section class="pt ref-text">
        <div class="ref-heading">
          <h2 data-glitch="PÁR REFERENCÍ">
            PÁR
            <span>REFERENCÍ</span>
          </h2>
        </div>
        <div class="spacer-lg"></div>
        <div class="spacer-lg"></div>
      </section>
      <div class="tabs">
        <div class="desktop">
          <div class="imac-tab">
            <div :style="{ backgroundImage: 'url(' + require('../assets/images/desktop-elim.png') + ')'}" class="screen">
            </div>
            <img src="~/assets/images/imac-stand-black.png" alt="">
          </div>
          <div class="imac-tab">
            <div :style="{ backgroundImage: 'url(' + require('../assets/images/desktop-ods.png') + ')'}" class="screen"></div>
            <img src="~/assets/images/imac-stand-black.png" alt="">
          </div>
          <div class="imac-tab">
            <div class="ref-showcase-text">
              <p>
                Několik vybraných projektů, na kterých jsem pracoval.
                <br/>
                Větší projekty realizujeme s naším týmem z <a href="htttps://maesty.co">maesty.co</a>
              </p>
            </div>
          </div>
          <div class="imac-tab">
            <div :style="{ backgroundImage: 'url(' + require('../assets/images/desktop-arched.png') + ')'}" class="screen"></div>
            <img src="~/assets/images/imac-stand-black.png" alt="">
          </div>
          <div class="imac-tab">
            <div :style="{ backgroundImage: 'url(' + require('../assets/images/desktop-maesty.png') + ')'}" class="screen"></div>
            <img src="~/assets/images/imac-stand-black.png" alt="">
          </div>
          <div class="imac-tab">
            <div :style="{ backgroundImage: 'url(' + require('../assets/images/desktop-kofola.png') + ')'}" class="screen"></div>
            <img src="~/assets/images/imac-stand-black.png" alt="">
          </div>
        </div>
      </div>
    </div>
    <div class="ppl-references pt">
      <div class="they-said">
        <h4>ŘEKLI O MNĚ</h4>
      </div>
      <div class="spacer-lg"></div>
      <div class="spacer-sm"></div>
      <div class="they-said-m">
        <div class="slideshow-container">
          <a class="prev" onclick="plusSlides(-1)"><img src="~/assets/images/arrow-left.svg" alt=""></a>
          <div class="mySlides fade first-slide">
            <div class="text">
              „Pavel je velice cílevědomý a snaživý,
              má opravdu veliký zápal pro svou práci,
              která ho velice baví. Pokora a důslednost jsou slova,
              která ho charakterizují,
              rozhodně doporučuji jeho služby.“
            </div>
            <div class="spacer-lg"></div>
            <div class="they-said-ppl">
              <p>Jan Wolinger,</p>
              <p style="visibility: hidden">P</p>
              <p>Product designer</p>
            </div>
            <div class="spacer-lg"></div>
          </div>
          <div class="mySlides fade">
            <div class="text">
              „K práci přistupuje tak, že se snaží s každým
              dalším projektem posunout o něco kousek dál.
              Svou práci vždy dotáhne dokonce.“
            </div>
            <div class="spacer-lg"></div>
            <div class="they-said-ppl">
              <p>Petr Víteček,</p>
              <p style="visibility: hidden">P</p>
              <p>Neat Solution, s.r.o</p>
            </div>
            <div class="spacer-lg"></div>
          </div>
          <!--<div class="mySlides fade">
            <div class="text">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit.
              Itaque laboriosam dolorum ipsa optio sapiente in exercitationem
              numquam facilis magnam suscipit totam asperiores dignissimos
              amet nostrum repudiandae officia quibusdam.
            </div>
            <div class="spacer-lg"></div>
            <div class="they-said-ppl">
              <p>lorem ipsum,</p>
              <p style="visibility: hidden">P</p>
              <p>lorem ipsum</p>
            </div>
            <div class="spacer-lg"></div>
          </div>-->
          <a class="next" onclick="plusSlides(1)"><img src="~/assets/images/arrow-right.svg" alt=""></a>
        </div>
        <br>
        <div class="slide-dots">
          <div class="dot-container" onclick="currentSlide(1)">
            <span class="dot active"></span>
          </div>
          <div class="dot-container" onclick="currentSlide(2)">
            <span class="dot"></span>
          </div>
          <!--<div class="dot-container" onclick="currentSlide(3)">
            <span class="dot"></span>
          </div>-->
        </div>
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
          content: 'referance'
        }
      ]
    }
  },
  data(){
    return {
      backgroundUrl:require('~/assets/images/imac-stand.png')
    }
  }
}

</script>
<style scoped lang="stylus">

.references
  position relative


.ref-heading
  max-width 556px
  margin 0 0 0 auto


.ref-showcase-text
  max-width initial
  text-align right


.ref-showcase-text p
  font-size 18px
  line-height 1.78
  letter-spacing -0.38px
  color #c1cedc


/* TABS */

.desktop
  display flex
  flex-wrap wrap

  .imac-tab
    width 33.33%
    transform scale(.85)

    .screen
      padding 25%
      border 12px solid #222222
      border-top-left-radius 15px
      border-top-right-radius 15px
      background-position top
      background-size cover
      transition 10s linear
      &:hover
        background-position bottom
        transition 6s linear


    img
      width 100%

/* TABS END */

.they-said
  max-width 1232px
  width 100%
  margin 0 auto
  h4
    letter-spacing -0.75px
    text-align center

.they-said-ppl
  display flex
  justify-content center
  p
    font-family ITCAvantGardePro-Md, sans-serif
    &:first-child
      color #df1a4a

.they-said-m
  position relative
  max-width 1232px
  width 100%
  margin 0 auto

.mySlides
  display none

.first-slide
  display block

.slideshow-container
  position relative
  display flex

.prev,
.next
  cursor pointer
  color white
  font-weight bold
  transition 0.6s ease
  border-radius 0 3px 3px 0
  width 50%

.prev
  text-align left
  align-self center
  padding-right 48px

.prev img, .next img
  width 100%

.next
  border-radius 3px 0 0 3px
  text-align right
  align-self center
  padding-left 48px

.text
  width 100%
  text-align center
  font-size 32px
  font-style italic
  line-height 1.69
  letter-spacing -0.67px
  color #c1cedc

.numbertext
  color #f2f2f2
  font-size 12px
  padding 8px 12px
  position absolute
  top 0

.slide-dots
  display flex
  justify-content space-evenly

.dot-container
  margin -16px
  padding 16px

.dot
  cursor pointer
  height 13px
  width 13px
  background-color #c1cedc
  border-radius 50%
  display inline-block
  transition background-color 0.6s ease

.active,
.dot:hover
  background-color #df1a4a
  border 1px solid white

.fade
  -webkit-animation-name fade
  -webkit-animation-duration 1.5s
  animation-name fade
  animation-duration 1.5s

@-webkit-keyframes fade
  from
    opacity .4

  to
    opacity 1

@keyframes fade
  from
    opacity .4

  to
    opacity 1

@media (max-width: 1150px)

  .red-black
    transform translateY(-185px)

  .blue
    transform translateY(-110px) scale(0.85)

@media (max-width: 950px)

  .tabs
    flex-direction column

  .tab
    transform unset

  .red-black
    > :not(:first-child)
      margin-top 32px

  .blue-green
    > *
      margin-top 32px

  .ods
    margin-top 32px

  .red-black, .blue
    transform unset

  .blue-green
    flex-direction column

  .bg-div
    max-width unset
    transform unset
    max-height 441px

  .kofola
    transform unset

  .ppl-references
    transform unset
    padding 80px 0

  .slideshow-container
    flex-direction column
    .next, .prev
      display none

  .text
    font-size 20px


@media (min-width: 950px)

  .slide-dots
    display none


</style>
