<template>
  <div class="charts-wrap">
    
    <el-button type="text" @click="getData(1)">数据1</el-button>

    <el-button type="text" @click="getData(2)">数据2</el-button>

    <EchartsBar :echartsData="echartsData" @handleCharts="handleCharts"></EchartsBar>

    <div class="text">{{text}}</div>
  </div>


</template>

<script type="text/javascript">
  import EchartsBar from 'components/echarts/bar'
  export default {
    name: 'home',
    data(){
      return {             
        echartsData:{
          xdata:['1月','2月','3月','4月','5月'],
          data:[100,200,300,400,500]
        },
        text:"",
      }
    },
    created(){
      
    },
    methods:{
      handleCharts(data){
        this.text = data;
      },
      getData(flag) {
        const echartsData1 = {
          xdata:['1月','2月','3月','4月','5月'],
          data:[100,200,300,400,500]
        }
        const echartsData2= {
          xdata:['1月','2月','3月','4月','5月'],
          data:[200,100,500,100,300]
        }
         this.echartsData = flag === 1 ? echartsData1 : echartsData2
      }
    },
    components:{
      EchartsBar
    }

   }
</script>

<style lang="scss" scoped>
  @import "~assets/css/lib-variable";
  @import "~assets/css/lib-mixin";
  .charts-wrap{
    width: 400px;
    height: 400px;
    .text{
      padding-left:30px;
      font-size:18px;
      color:#000;
    }
  }

</style>
