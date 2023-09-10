<script>
const echarts = require('../../public/echart.min.js')
 export default {
   mounted() {
     this.loadData()
   },
   methods: {
     loadData() {
       // 发起get请求，真实场景中将路径更换为webapi地址
       this.$http.get('gcb.json', {})
         .then((res) => {
           // 输出读取到的数据
           console.log(res.data)
           const option = {
             title: {
               text: '新冠数据统计'
             },
             legend: {
               data: ['Email', 'Union Ads', 'Video Ads']
             },
             xAxis: {
               type: 'category',
               boundaryGap: false,
               data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
             },
             yAxis: {
               type: 'value'
             },
             series: [
               {
                 name: 'Email',
                 type: 'line',
                 stack: 'Total',
                 data: [120, 132, 101, 134, 90, 230, 210]
               },
               {
                 name: 'Union Ads',
                 type: 'line',
                 stack: 'Total',
                 data: [220, 182, 191, 234, 290, 330, 310]
               },
               {
                 name: 'Video Ads',
                 type: 'line',
                 stack: 'Total',
                 data: [150, 232, 201, 154, 190, 330, 410]
               }
             ]
           }
           // 第4步：生成数据
           var legendArr = ['累计确诊总数', '累计出院', '接受医学观察']
           var xaxisArr = []
           var ljqzzsArr = []
           var ljcyArr = []
           var jsyxgcArr = []
           var dataArr = res.data.data
           for (var i = 0; i < dataArr.length; i++) {
             xaxisArr.push(dataArr[i].jzrq)
             ljqzzsArr.push(dataArr[i].ljqzzs)
             ljcyArr.push(dataArr[i].ljcy)
             jsyxgcArr.push(dataArr[i].jsyxgc)
           }
           // 第5步：更新配置
           option.legend.data = legendArr
           option.xAxis.data = xaxisArr
           option.series[0].name = '累计确诊总数'
           option.series[0].data = ljqzzsArr
           option.series[1].name = '累计出院'
           option.series[1].data = ljcyArr
           option.series[2].name = '接受医学观察'
           option.series[2].data = jsyxgcArr
           var chartDom = document.getElementById('main')
           var myChart = echarts.init(chartDom)
           myChart.setOption(option)
         })
     }
   }
 }
 </script>