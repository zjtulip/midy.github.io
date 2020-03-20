<template>
  <div class="main">
    <div class="sub">
      <div class="conent">
        <Content></Content>
      </div>
      <div class="sidebar">
        <Sidebar></Sidebar>
      </div>
    </div>
  </div>
</template>

<script>
import Sidebar from './sidebar'
import Content from './content'
export default {
  name: 'main',

  components: {
    Sidebar,
    Content
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
  .main
    width 86%
    height 80%
    border 16px solid #fddada !important
    border-radius 40px
    background-color #fddada
    box-shadow 8px 8px 16px #FBB8B7
    .sub
      background-color #fdfdfd
      border-radius 30px
      height 100%
      display flex
      .conent
        flex 1
        width 70%
        // background-color #fdfdfd
        // outline 1px solid #f00
      .sidebar
        width 280px
        // width 30%
        background-color #fff
        border 18px solid #fff !important
        border-radius 30px
        box-shadow 1px 3px 16px #e2e2e5
        // outline 1px solid #f00
</style>


