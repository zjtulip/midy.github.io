<template>
  <div class="services">
    <div class="topban">
      <span>View all</span>
      <h2>Main Services</h2>
    </div>
    <ul class="serlist">
      <li>
        <i class="el-icon-set-up"></i>
        <p>Transtions</p>
      </li>
      <li>
        <i class="el-icon-sunrise-1"></i>
        <p>Utility</p>
      </li>
      <li>
        <i class="el-icon-copy-document"></i>
        <p>Loans</p>
      </li>
      <li>
        <i class="el-icon-news"></i>
        <p>Deposhts</p>
      </li>
      <li>
        <i class="el-icon-bangzhu"></i>
        <p>Fasttansfer</p>
      </li>
      <li>
        <i class="el-icon-refresh"></i>
        <p>Exchange</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'services',

  components: {
  },

  mounted () {
  },

  methods: {
  }
}
</script>

<style lang="stylus" scoped>
  .services
    .topban
      overflow hidden
      span
        float right
        color #d7d7db
        line-height 0.15rem
      h2
        font-size 0.12rem
        color #1f2e44
    .serlist
      display flex
      flex-flow row wrap
      justify-content space-between
      margin 20px 0
      // min-width 200px
      overflow hidden
      li
        // float left
        background-color #fff
        border-radius 20px
        padding 10px 4px 8px
        margin 0 12px 24px 0px
        text-align center
        box-shadow 6px 6px 10px #e2e2e5
        min-width 100px
        i
          font-size 0.2rem
          color #ff6f76
        p
          color #14233c
          opacity 0.8
          font-size 8px
</style>
