<template>
  <div v-if="loading" class="loading-page">
    <div class="background">
      <div class="load-con">
        <div class="loader">
          <div class="outer"></div>
          <div class="inner"></div>
        </div>
        <div class="progress-bar">
          <div class="bar" data-size="100">
            <span style="color: white;" class="perc"></span>
          </div>
        </div>
        <h3></h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    loading: false
  }),
  methods: {
    start () {
      this.loading = true
    },
    finish () {
      this.loading = false
    }
  },
  mounted() {
    function loading() {
      document.querySelectorAll(".bar").forEach(function(current) {
      let startWidth = 0;
      const endWidth = current.dataset.size;

    /*
    setInterval() time sholud be set as trasition time / 100.
    In our case, 2 seconds / 100 = 20 milliseconds.
    */
    const interval = setInterval(frame, 60);

    function frame() {
      if (startWidth >= endWidth) {
        clearInterval(interval);
      } else {
          startWidth++;
          current.style.width = `${endWidth}%`;
          current.firstElementChild.innerText = `${startWidth}%`;
        }
     }
  });
}

setTimeout(loading, 1000);
  }
};
</script>

<style scoped lang="stylus">

.loading-page
  position fixed
  z-index 999
  top 0
  left 0
  width 100%
  height 100%
  background rgba(0, 0, 0, 1)
  text-align center
  display flex
  justify-content center
  align-items center
  animation opacity 9s ease


.background
  width 100%
  height 100vh
  background linear-gradient(90deg, #0f1927 0, #2a3545 100%)
  position relative
  transition 1s ease
  display flex
  justify-content center
  align-items center


.load-con
  width 100%
  max-width 300px


.progress-bar
  height 30px
  margin 32px 0
  background-color black
  border-radius 20px
  overflow hidden
  box-shadow 2px 0 10px inset rgba(0,0,0,0.2)
  position relative


.bar
  width 0
  height 100%
  background-color #df1a4a
  background-size 30px 30px
  box-shadow 2px 0 10px inset rgba(0,0,0,0.2)
  transition width 6s ease-out


.perc
  position absolute
  top 50%
  left 50%
  transform translate(-50%, -50%)
  color #fff
  font-weight bold


.loader
  position relative
  display flex
  justify-content center
  align-items center

  .outer
    border 5px solid white
    opacity .9
    border-right-color transparent
    border-left-color transparent
    width 70px
    height 70px
    border-radius 50%
    box-shadow 0 0 35px #df1a4a
    animation spin-pulse 1s linear infinite

  .inner
    border 5px solid white
    opacity .9
    border-left-color transparent
    border-right-color transparent
    border-radius 50%
    box-shadow 0 0 15px #df1a4a
    width 40px
    height 40px
    position absolute
    animation spin-right 3s linear infinite


h3
  &::before
    content "Vytvářím aplikaci, prosím o strpení"
    animation text 1s linear forwards
    animation-delay 6.5s

@keyframes spin-pulse

  from
    transform rotate(160deg)
    box-shadow0 0 1px red

  50%
    transform rotate(145deg)

  to
    transform rotate(-320deg)


@keyframes spin-right

  from
    transform rotate(0deg)

  50%
    transform rotate(180deg)

  to
    transform rotate(360deg)

@keyframes text

  0%
    content "Vytvářím aplikaci, prosím o strpení"

  100%
    content "Hotovo"

@keyframes opacity
  0%
    opacity 1
  50%
    opacity 1
  75%
    opacity 1
  90%
    opacity 1
  100%
    opacity 0

@media (max-width: 1100px)

  .background
    &::after
      font-size 80px


@media (max-width: 950px)

  .background
    &::before
      width calc(100% - 48px)
    &::after
      font-size 38px

</style>
