<template>
  <div class="current">
    <div class="topban">
      <span>View all</span>
      <h2>Current</h2>
    </div>
    <ul class="clists">
      <li>
        <div class="nums">1063873637834</div>
        <div class="line"></div>
        <div class="moneys">$2,200.01</div>
      </li>
      <li>
        <div class="nums">1063873633467</div>
        <div class="line"></div>
        <div class="moneys">$1,300.89</div>
      </li>
      <li>
        <div class="nums">1063873639987</div>
        <div class="line cs1"></div>
        <div class="moneys">$1,848.11</div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'current',

  components: {
  },

  mounted () {
  },

  methods: {
    
  }
}
</script>

<style lang="stylus" scoped>
  .current
    .topban
      overflow hidden
      span
        float right
        color #d7d7db
        line-height 0.15rem
      h2
        font-size 0.12rem
        color #1f2e44
    .clists
      margin 20px 0
      li
        display flex
        font-size 16px
        justify-content space-between
        line-height 40px
        .nums
          color #b7b9bf
          margin-right 10px
        .moneys
          color #1a2433
          margin-left 10px
        .line
          border-bottom 1px dashed #e2ece9
          height 24px
          flex 1
.cs1
  border-bottom 1px dashed #ccddd8 !important
</style>