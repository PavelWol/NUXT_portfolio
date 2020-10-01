<template>
  <div class="pt footer-container">
    <div class="footer-heading">
      <h2 data-glitch="NEVÁHEJTE MĚ KONTAKTOVAT">
        NEVÁHEJTE MĚ
        <span>KONTAKTOVAT</span>
      </h2>
    </div>
    <div class="spacer-lg"></div>
    <div class="spacer-lg"></div>
    <section class="contact-form">
      <form method="post"> <!--action="mailhandler.php"-->
        <div class="fields">
          <div class="full">
            <div class="half">
              <!-- <label for="first_name">Jméno</label> -->
              <input placeholder="Jméno" type="text" name="first_name" id="first_name" />
            </div>
            <div class="spacer-md"></div>
            <div class="half">
              <!-- <label for="email">Email</label> -->
              <input placeholder="Email" type="text" name="email" id="email" />
            </div>
            <div class="spacer-md"></div>
          </div>
          <div class="field">
            <!-- <label for="message">Vaše zpráva</label> -->
            <textarea placeholder="Vaše zpráva" name="message" id="message" rows="6"></textarea>
          </div>
          <div class="spacer-md"></div>
          <input
          type="submit"
          name="submit"
          class="submit"
          value="Odeslat"
          />
        </div>
      </form>
      <section class="socials">
        <a href="mailto:pw.wolinger@gmail.com">
          <img src="~/assets/images/email.png" alt="">
          <p>pw.wolinger@gmail.com</p>
        </a>
        <div class="spacer-lg"></div>
        <a href="tel:+420 777 051 053">
          <img src="~/assets/images/phone.png" alt="">
          <p>+420 777 051 053</p>
        </a>
        <div class="spacer-lg"></div>
        <a href="">
          <img src="~/assets/images/facebook.png" alt="">
          <p>Facebook</p>
        </a>
        <div class="spacer-lg"></div>
        <a href="">
          <img src="~/assets/images/github.png" alt="">
          <p>Github</p>
        </a>
      </section>
    </section>
  </div>
</template>

<script>

export default {
  name: 'Footer',

  head() {
      return {
        title: 'Kontakt',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'kontakt'
          }
        ]
      }
    }

}

</script>

<style scoped lang="stylus">

footer
  position relative


.rectanglefot
  position absolute
  right 0
  top 54%


.rectanglefot img
  animation sink 4s ease-in-out infinite


.rectanglefot2
  position absolute
  z-index -1
  right 27%
  top -35%


.rectanglefot2 img
  animation sink 4s ease-in-out infinite


.rectanglefot3
  position absolute
  top 27%
  left 70px


.rectanglefot3 img
  animation right 4s ease-in-out infinite


.rectanglefot4
  position absolute
  top 52%
  right -25%


.rectanglefot4 img
  animation left 4s ease-in-out infinite


.ovalfot
  position absolute
  right 10%
  bottom 50%


.ovalfot img
  animation rotate 6s ease-in-out infinite


.dotsfot
  position absolute
  left 38%
  bottom 17%


.dotsfot img
  animation sink 6s ease-in-out infinite
  width 50%


.footer-container
  max-width 1232px
  width 100%
  margin 0 auto
  position relative


.footer-heading
  margin 0 0 0 auto
  position relative


.footer-heading h2
  line-height 1.09
  letter-spacing -4.13px
  position relative


.footer-heading h2 span
  color #df1a4a
  display block


.contact-form
  display flex
  justify-content space-between
  flex-direction row-reverse


.contact-form form
  width 60%

.fields
  max-width 584px
  margin 0 0 0 auto

div.half
  position relative


div.half input
  width 100%
  height 72px
  padding 0 24px
  box-shadow 0 32px 49px 0 rgba(18, 26, 39, 0.32)
  border solid 1px rgba(255, 255, 255, 0.1)
  background-color #131c2b
  border-radius 3px
  color #ffffff


div.half input:focus, div.field textarea:focus
  outline none
  /*border 1px solid var(--main-color) */
  /*filter drop-shadow(0 0 0.75rem var(--main-color)) */


.field
  position relative


div.field textarea
  width 100%
  height 178px
  padding 28px 24px 28px 24px
  box-shadow 0 32px 49px 0 rgba(18, 26, 39, 0.32)
  border solid 1px rgba(255, 255, 255, 0.1)
  background-color #131c2b
  resize none
  border-radius 3px
  color #ffffff


input.submit
  width 100%
  height 72px
  color #ffffff
  outline none
  border:solid 1px rgba(223, 26, 74, 0.9)
  background-color #df1a4a
  -webkit-box-shadow 0 8px 0 0 #8b1330,
                      0 16px 32px 0 rgba(223, 26, 74, 0.22)
  -moz-box-shadow 0 8px 0 0 #8b1330,
                   0 16px 32px 0 rgba(223, 26, 74, 0.22)
  box-shadow 0 8px 0 0 #8b1330,
              0 16px 32px 0 rgba(223, 26, 74, 0.22)
  cursor pointer


input.submit:active
  -webkit-box-shadow 0 4px 0 0 #8b1330,
                      0 16px 32px 0 rgba(223, 26, 74, 0.22)
  -moz-box-shadow 0 4px 0 0 #8b1330,
                   0 16px 32px 0 rgba(223, 26, 74, 0.22)
  box-shadow 0 4px 0 0 #8b1330,
              0 16px 32px 0 rgba(223, 26, 74, 0.22)
  position:relative
  top:7px


/* SOCIALS */

.socials
  width 40%

.socials
  a
    display flex
    align-items center
    text-decoration none


.socials
  img
    width 32px
    margin-right 32px


.socials p
  font-size 24px
  letter-spacing -1.13px
  align-self flex-end


@media (max-width: 950px)

  .contact-form
    flex-direction column
    form
      width 100%

  .socials
    width 100%
    padding 80px 0
    p
      font-size 20px

</style>

