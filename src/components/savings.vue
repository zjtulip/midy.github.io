<template>
  <div class="savings">
    <div class="topban">
      <span>View all</span>
      <h2>savings</h2>
    </div>
    <div class="savban">
      <div class="layout_echar1">
        <div id="echartline"></div>
      </div>
      <div class="layout_lists">
        <ul class="clists">
          <li>
            <div class="nums">Total</div>
            <div class="moneys">$100.01</div>
          </li>
          <li>
            <div class="nums">This week</div>
            <div class="moneys">$2,567.89</div>
          </li>
          <li>
            <div class="nums">This month</div>
            <div class="moneys">$123.11</div>
          </li>
        </ul>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'savings',

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
        let myChart = this.echarts.init(document.getElementById('echartline'))

        myChart.setOption({
            tooltip: {},
            xAxis: {
              type: 'category',
              axisLine: {show:false},
              axisTick: {show:false},
              data: ["$10", "$20", "$30", "$40", "$50"]
            },
            yAxis: {
              type: 'value',
              axisLine: {show:false},
              axisTick: {show:false},
              splitLine: {
                lineStyle:{
                    type:'dashed',
                    color: '#e2ece9'
                },
              },
            },
            grid: {
              show: false,
              left: '10%',
              right: '6%',
              top: '20%',
              bottom: '20%',
              borderColor: '#f00',
              borderWidth: 2,
              lineStyle: {
                  type:'dashed'
                }
            },
            series: [{
                type: 'line',
                smooth: true,
                symbolSize: 8,
                color: '#44b5cf',
                lineStyle:{ width: 4, color: '#44b5cf'},
                data: [15, 70, 26, 160, 206]
            }]
        });
    }
  }
}
</script>

<style lang="stylus" scoped>
  .savings
    .topban
      overflow hidden
      span
        float right
        color #d7d7db
        line-height 0.15rem
      h2
        font-size 0.12rem
        color #1f2e44
    .savban
      display flex
      .layout_echar1
        flex 1
        // outline 1px solid #f00
      .layout_lists
        width 200px
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
#echartline
  width 100%
  height 200px
  // border 1px solid #000
</style>