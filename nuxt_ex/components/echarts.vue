<template>
  <div class="echarts_box">
    <p class="title">
      <span>直播实际开始于 {{start_time}} - 实际结束于 {{end_time}}</span>
      <span>直播开始人数：{{start_people_num}}人</span>
      <span>最高在线人数：{{max_people_num}}人</span>
      <span>直播结束人数：{{end_people}}人</span>
      <span>平均在线时长：{{average_time}}分钟</span>
    </p>
    <div id="myChart" :style="{width: '2400px', height: '300px'}"></div>
  </div>
</template>


<script>
// 引入基本模板
let echarts = require('echarts/lib/echarts')
// 引入柱状图组件
require('echarts/lib/chart/line')
// 引入提示框和title组件
require('echarts/lib/component/tooltip')
require('echarts/lib/component/title')
require('echarts/lib/component/legend')
export default {
  name: 'Echarts',
  data(){
    return{
      start_time: '2018-08-10 16:32',
      end_time: '2018-08-10 16:33',
      start_people_num: 256,
      max_people_num: 270,
      end_people: 110,
      average_time: 65.6
    }
  },
  mounted() {
    this.drawLine();
  },
  methods: {
    drawLine() {
      // 基于准备好的dom，初始化echarts实例
      let myChart = echarts.init(document.getElementById('myChart'))
      // 绘制图表
      myChart.setOption({
        backgroundColor: '#eee',
        legend: {
          data: ['直播人数']
        },
        xAxis: {
          boundaryGap: false,
          splitLine: {
              show: true
          },
          axisLabel:  {
              margin: 20
          },
          data: ["19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30", "19：57", "20：01", "20：30", "21：00", "22：11", "23：30"]
        },
        yAxis: {
          type: 'value',
          minInterval: 1,
          splitLine: {
              show: true
          },
          axisLabel:  {
              margin: 10
          },
        },
        series: [{
          name: '直播人数',
          type: 'line',
          itemStyle: {
              color: '#0a8bcd',
          },
          data: [0, 5, 2, 2, 4, 5, 5, 2, 2, 2, 4, 5]
        }],
        axisTick: [{
          show: false,
          boundaryGap: true
        }],
        grid: [{
            show: true,
            left: 30,
            top: 40,
            right: 30,
            bottom: 10,
            containLabel: true,
        }],
        tooltip: [{
          trigger: 'axis',
          confine: true,
          formatter: '2018-10-27  {b}<span style="display:block;width:100%;height:1px;background:#fff;margin-bottom:10px"></span>直播: <span style="margin-left:80px">{c}</span>'
        }]
      });
    }
  }
}
</script>

<style lang="less" scoped>
.echarts_box{
  overflow-x: scroll;
  .title{
    font-size: 14px;
    color: #99999f;
    display: flex;
    span{
      display: block;
    }
    span+span{
      margin-left: 20px;
    }
  }
}
</style>
