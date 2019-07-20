<template>
  <fusioncharts
        :type="type"
        :width="width"
        :height="height"
        :dataFormat="dataFormat"
        :dataSource="dataSource">
  </fusioncharts>
</template>
<script>
  //import LineChart from '@/components/charts/LineChart.js'
  export default {
    name: 'LineChartContainer',
    //components: { LineChart },
    props: ['dataSource'],
    data(){
      return {
          type: 'column2d', // The chart type
          width: '100%', // Width of the chart
          height: '100%', // Height of the chart
          dataFormat: 'json', // Data type
      }
    },
  }
</script>
