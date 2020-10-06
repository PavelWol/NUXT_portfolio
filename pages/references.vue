<template>
  <div class="">
    <div class="references">
      <section class="pt ref-text">
        <div class="ref-heading">
          <h2 data-glitch="MOJE REFERENCE">
            MOJE
            <span>REFERENCE</span>
          </h2>
        </div>
        <div class="spacer-lg"></div>
        <div class="spacer-lg"></div>
        <div class="ref-showcase-text">
          <p>
            Ukázky několika vybraných projektů, které
            jsme vytvářeli s týmem maesty.co.
          </p>
        </div>
      </section>
      <div class="tabs">
        <div class="red-black">
          <div class="tab red">
            <a target="_blank" href="http://maesty.co" class="bg-div bg-div-red">
              <img src="~/assets/images/red.png" alt="" />
              <div class="tabs-text">
                <h3>MAESTY</h3>
                <p>Digitální studio</p>
              </div>
            </a>
          </div>
          <div style="display: none;" class="tab black">
            <a class="bg-div bg-div-black">
              <img src="~/assets/images/black.png" alt="" />
              <div class="tabs-text">
                <h3>REACT APP</h3>
                <p>Testovaci projekt</p>
              </div>
            </a>
          </div>
          <a target="_blank" href="https://kdevonikofola.cz/" class="bg-div bg-div-green kofola">
            <img src="~/assets/images/map-service.png" alt="" />
            <div class="tabs-text">
              <h3>Kofola</h3>
              <p>Kde voní kofola</p>
            </div>
          </a>
        </div>
        <div class="blue-green">
          <div class="tab blue">
            <a target="_blank" href="http://www.arched.cz" class="bg-div bg-div-blue">
              <img src="~/assets/images/blue.png" alt="" />
              <div class="tabs-text">
                <h3>ARCHED</h3>
                <p>Portfolio architekta</p>
              </div>
            </a>
            <a target="_blank" href="https://www.modryplan.cz/" class="bg-div bg-div-red ods">
              <img src="~/assets/images/ods-web.png" alt="" />
              <div class="tabs-text">
                <h3>ODS</h3>
                <p>Krajské volby 2020</p>
              </div>
            </a>
          </div>
          <div class="tab green">
            <a target="_blank" href="http://www.cirkevelim.cz/" class="bg-div bg-div-green">
              <img src="~/assets/images/green.png" alt="" />
              <div class="tabs-text">
                <h3>ELIM</h3>
                <p>Cirkevni web</p>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="ppl-references">
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
              <p>Product designer</p>
            </div>
            <div class="spacer-lg"></div>
          </div>
          <div class="mySlides fade">
            <div class="text">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit.
              Cumque temporibus necessitatibus iste! Quis eaque eos sit,
              veritatis dolore ea quia voluptate illo minima molestiae earum!
            </div>
            <div class="spacer-lg"></div>
            <div class="they-said-ppl">
              <p>Vojtěch Fišar,</p>
              <p>Twitch streamer</p>
            </div>
            <div class="spacer-lg"></div>
          </div>
          <div class="mySlides fade">
            <div class="text">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit.
              Itaque laboriosam dolorum ipsa optio sapiente in exercitationem
              numquam facilis magnam suscipit totam asperiores dignissimos
              amet nostrum repudiandae officia quibusdam.
            </div>
            <div class="spacer-lg"></div>
            <div class="they-said-ppl">
              <p>Melichar Humáč,</p>
              <p>Lorem ipsumáč</p>
            </div>
            <div class="spacer-lg"></div>
          </div>
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
          <div class="dot-container" onclick="currentSlide(3)">
            <span class="dot"></span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

export default {
  head() {
    return {
      title: 'Reference',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'referance'
        }
      ]
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
  max-width 330px
  margin 0 0 0 auto
  margin-bottom 10%


.ref-showcase-text p
  font-size 18px
  line-height 1.78
  letter-spacing -0.38px
  color #c1cedc


.tabs
  display flex
  justify-content center


.tab
  position relative
  transform scale(.85)


.bg-div
  height 100%
  position relative
  overflow hidden
  cursor pointer
  max-width 361px
  width 100%
  max-height 440px
  display block


.bg-div img
  width 100%
  transition all .3s


.bg-div:hover img
  opacity .5
  transition all .3s


.tabs-text
  position absolute
  bottom 20%
  left 22%


.tabs-text2
  position absolute
  bottom 60%
  left 22%


.tabs-text h4, .tabs-text2 h4
  letter-spacing -1.13px


.tabs-text p, .tabs-text2 p
  font-size 18px
  line-height 1.78
  letter-spacing -0.38px


.ods .future-img
  width 361px
  height 440px
  background-color #df1a4a


.kofola
  transform scale(.85)
  .tabs-text
    *
      color black


.kofola .future-img
  width 361px
  height 440px
  background-color #37E8DB



.red-black
  display flex
  flex-direction column
  transform:translateY(-390px)


.red
  width 100%
  /* padding-right 40px  */
  /* background-image url('../img/bg/red.png')
  background-repeat no-repeat
  background-size cover
  background-position center  */

/*

.bg-div-red
  background-position 0
  background-size 303% 303% !important
  transition all 1s
  background linear-gradient(180deg, black 33%, white 33%, white 66%, #df1a4a 66%)


.bg-div-black
  background-position 0
  background-size 303% 303% !important
  transition all 1s
  background linear-gradient(180deg, black 33%, white 33%, white 66%, #1B2534 66%)


.bg-div-green
  background-position 0
  background-size 303% 303% !important
  transition all 1s
  background linear-gradient(180deg, black 33%, white 33%, white 66%, #37E8DB 66%)


.bg-div-blue
  background-position 0
  background-size 303% 303% !important
  transition all 1s
  background linear-gradient(180deg, black 33%, white 33%, white 66%, #37B6E8 66%)


*/

.bg-div:after
  background #df1a4a
  width 100%
  height 100%
  position absolute
  top 50%
  left 50%
  content ''
  opacity 0.75
  -webkit-transform skew(-45deg) scaleX(0)
  transform translate(-50%, -50%) skew(-45deg) scaleX(0)
  -webkit-transition all 0.3s ease-in-out
  transition all 0.3s ease-in-out


.bg-div-black:after
  background #000000


.bg-div-blue:after
  background #37B6E8


.bg-div-green:after
  background #37E8DB


.bg-div:hover:after
  -webkit-transform skew(-45deg) scaleX(1)
  transform translate(-50%, -50%) skew(-45deg) scaleX(1)
  transition all 400ms cubic-bezier(0.175, 0.885, 0.32, 1.275)


.ods
  transform translateY(68px)

.bg-div .tabs-text h3
  position relative
  z-index 1
  font-family ITCAvantGardeProBold, sans-serif
  font-size 20px

.bg-div .tabs-text p
  opacity 0
  transition all .3s
  position relative
  z-index 1


.bg-div:hover .tabs-text p
  opacity 1
  transition all .3s


.black
  width 100%
  /* padding-top 80px
  padding-right 40px  */



.blue-green
  display flex
  height 50%


.blue
  /* padding 0 40px  */
  transform:translateY(-210px) scale(.85)
  width 100%


.green
  /* padding-left 40px  */
  width 100%

.ppl-references
  transform translateY(-25%)

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
