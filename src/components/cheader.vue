<template>
  <div class="cheader">
    <div class="logo">
      <img src="../../static/img/mlogo.png">
    </div>
    <ul class="mlink">
      <li class="current">Dashboard</li>
      <li>Services</li>
      <li>History</li>
      <li>Actions</li>
    </ul>
    <div class="csearch">
      <input class="search_Input" type="text" placeholder="search...">
      <i class="el-icon-search search_icon"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'cheader',

  components: {
  },

  mounted () {
  },

  methods: {
  }
}
</script>

<style lang="stylus" scoped>
  .cheader
    display flex
    .mlink
      overflow hidden
      display flex
      flex-direction row
      margin 22px 60px 0 50px
      li
        margin 0 24px 0
        color #91939e
      .current
        color #17263f
      :hover
        color #17263f
    .csearch
      // width 220px
      background-color #f8f8f8
      border 1px solid #f8f8f8
      border-radius 20px
      display flex
      justify-items center
      padding 0 20px 0 0px
      .search_Input
        border none
        background-color #f8f8f8
        border-radius 20px
        padding 0 20px 0 20px
        color #c7c8cd
      .search_icon
        font-size 18px
        margin 10px 0 0 0
        color #bcbec3
</style>
