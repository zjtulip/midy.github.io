<template>
  <div class="sidebar2">
    <div class="topban">
      <div class="user">Anastasia <span class="pic"><img src="../../static/img/person.png" ></span></div>
      <i class="el-icon-bell btn1">
        <span class="ras"></span>
      </i>
    </div>
    <div id="echartpie"></div>
    <div class="topban">
      <span class="fr">Today</span>
      <h2>Transactions</h2>
    </div>
    <ul class="clists">
      <li>
        <div class="cion"><i class="el-icon-pie-chart"></i></div>
        <div class="moneys">Dribbble Pro Plan</div>
        <div class="moneys ct1">-$100</div>
      </li>
      <li>
        <div class="cion"><i class="el-icon-data-analysis"></i></div>
        <div class="moneys">Adidas Refund&nbsp;&nbsp;&nbsp;&nbsp;</div>
        <div class="moneys ct2">+$230</div>
      </li>
      <li>
        <div class="cion"><i class="el-icon-grape"></i></div>
        <div class="moneys">Wacom LCD&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</div>
        <div class="moneys ct1">-$3000</div>
      </li>
    </ul>
    <div class="btnban">
      Transfer Money <i class="el-icon-right arbtn"></i>
    </div>
    <div class="wet">
      <i class="el-icon-chat-line-round"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'sidebar',

  components: {
  },

  mounted () {
    this.$nextTick(()=>{
      this.drawLine()
    })
  },
  updated() {
    this.drawLine()
  },
  methods: {
    drawLine(){
        let myChart = this.echarts.init(document.getElementById('echartpie'))

        myChart.setOption({
            tooltip: {},
             series: [{
              type: 'pie',
              radius: ['50%', '70%'],
              avoidLabelOverlap: false,
              label: {
                  show: false,
                  position: 'center'
              },
              emphasis: {
                  label: {
                      show: true,
                      fontSize: '20',
                      fontWeight: 'bold'
                  }
              },
              labelLine: {
                  show: true,
                  fontSize: '20',
                  fontWeight: 'bold'
              },
              color:['#F8F8F8','#14233C','#0e809A','#FF2934','#0e809A'],
              data: [
                  {value: 2349, name: 'Balance'},
                  {value: 2102, name: 'Aalmle'},
                  {value: 2345, name: 'Vense'},
                  {value: 2345, name: 'Rdnse'},
              ]
          }]
        });
    }
  }
}
</script>

<style lang="stylus" scoped>
  .sidebar2
    .topban
      overflow hidden
      color #1f2e44
      .fr
        float right
        color #d7d7db
        line-height 0.15rem
      h2
        font-size 0.01rem
        color #d7d7db
      .user
        float right
        color #d7d7db
        line-height 0.15rem
        .pic
          margin 0 0 0 10px
          width 20px
          height 20px
          border-radius 10px
          img
            width 34px
            height 34px
            border-radius 17px
      .btn1
        font-size 0.14rem
        color #d7d7db
        position relative
        .ras
          position absolute
          width 8px
          height 8px
          border-radius 4px
          background-color #f00
          left 16px
    .clists
      margin 20px 0
      li
        display flex
        font-size 16px
        justify-content space-between
        align-items flex-start
        line-height 70px
        .cion
          margin 8px 0 0 0
          padding 8px 10px
          border-radius 10px
          width 26px
          height 26px
          line-height 36px
          box-shadow 6px 6px 16px #e2e2e5
          // border 1px solid #f00
          i 
            color #FD5B63
            font-size 26px
        .nums
          color #b7b9bf
          margin-right 10px
        .moneys
          color #1a2433
          margin-left 10px
          align-items baseline
          justify-content flex-start
        .line
          border-bottom 1px dashed #e2ece9
          height 24px
          flex 1
.cs1
  border-bottom 1px dashed #ccddd8 !important
#echartpie
  width 100%
  height 300px
  margin 20px 0 5px
  // border 1px solid #000
.ct1 
  color #FF7981 !important
.ct2
  color #479DB2 !important
.btnban
  background-color #FF4D56
  width 76%
  height 42px
  border-radius 20px
  cousor pointer
  color #fff
  margin 10px auto
  opacity 0.8
  padding 0 20px
  line-height 42px
  overflow hidden
  .arbtn
    font-size 20px
    float right
    margin 12px 0 0 0
.wet
  width 40px
  height 40px
  border-radius 30px
  background-color #0e809A
  float right
  margin 20px 20px 0 0
  text-align center
  vertical-align middle
  i 
    color #ffffff
    font-size 0.13rem
    margin 8px auto
</style>