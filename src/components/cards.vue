<template>
  <div class="cards">
    <div class="topban">
      <span>View all cards</span>
      <h2>Cards</h2>
    </div>
    <div class="cardsban">
      <ul class="cardslist">
        <li>
          <div class="card">
            <p class="tit1">Amlabawned</p>
            <p class="money">$2,200</p>
            <p class="num">**** **** **** **34</p>
            <p class="money">Monzo</p>
            <p class="ruy1 cred1"></p>
            <p class="ruy2"></p>
          </div>
        </li>
         <li>
          <div class="card cbule1">
            <p class="tit1">Amlabawned</p>
            <p class="money">$1,300,89</p>
            <p class="num">**** **** **** **67</p>
            <p class="money">Monzo</p>
            <p class="ruy1 cred2"></p>
            <p class="ruy2"></p>
          </div>
        </li>
        <li>
          <div class="card cgrey">
            <i class="el-icon-circle-plus-outline addbtn"></i>
            <p class="add">Add New Card</p>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'cards',

  components: {
  },

  mounted () {
  },

  methods: {
    
  }
}
</script>

<style lang="stylus" scoped>
  .cards
    margin 40px 0
    width 100%
    .topban
      overflow hidden
      span
        float right
        color #d7d7db
        line-height 0.15rem
      h2
        font-size 0.12rem
        color #1f2e44
    .cardsban
      margin 20px 0
      .cardslist
        width 100%
        overflow hidden
        li
          float left
          width 28%
          margin 0 5% 0 0
          .card
            background-color #ff4d56
            border-radius 20px
            padding 20px 20px 0
            position relative
            color #a1a2ab
            min-height 150px
            .tit1
              font-size 0.001rem
              opacity 0.4
              transform: scale(1, 0.6);
              -webkit-transform: scale(1, 0.6);
              -moz-transform: scale(1, 0.6);
              -o-transform: scale(1, 0.6);
            .money
              color #fff
              padding 0 0 22px 0
              margin 0
            .num
              color #1f2e44
              opacity 0.4
            .ruy1
              position absolute
              bottom 5px
              right 34px
              width 28px
              height 28px
              border-radius 14px
              background-color #e30613
            .ruy2
              position absolute
              bottom 5px
              right 14px
              width 28px
              height 28px
              border-radius 14px
              background-color #ffc24b
            .addbtn
              font-size 0.3rem
              color #d8d8d8
            .add
              margin-bottom 28px
.cred1
  background-color #e30613 !important
.cred2
  background-color #ff3a4f !important
.cbule1
  background-color #0e809a !important
.cgrey
  background-color #f8f8f8 !important
  display flex
  flex-direction column
  justify-content center
  align-items center
</style>
