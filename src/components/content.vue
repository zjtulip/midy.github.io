<template>
  <div class="subcontent">
    <Cheader></Cheader>
    <Cards></Cards>
    <div class="layout3">
      <div class="lservices">
        <Services></Services>
      </div>
      <div class="les">
        <Current></Current>
        <Savings></Savings>
      </div>
    </div>
  </div>
</template>

<script>
import Cheader from './cheader'
import Cards from './cards'
import Services from './services'
import Current from './current'
import Savings from './savings'
import Nav from './Nav'
export default {
  name: 'content',

  components: {
    Cheader,
    Cards,
    Services,
    Current,
    Savings,
    Nav
  },

  mounted () {
    this.init()
  },

  methods: {
    init () {
      this.Adaptive()
      window.onresize = () => {
        this.Adaptive()
      }
    },

    Adaptive () {
      document.querySelector('html').style.fontSize = `${document.querySelector('html').offsetWidth / 10}px`
    }
  }
}
</script>

<style lang="stylus" scoped>
  .subcontent
    padding 40px 60px
    .layout3
      display flex
      direction row
      .lservices
        width 24%
        // width 320px
        // outline 1px solid #f00
      .les
        flex 1
        width 70%
        margin 0 0 0 40px
        // outline 1px solid #000
</style>
