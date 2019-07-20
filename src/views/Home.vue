<template>
	<div class="home">
		<barChart :dataSource="dataSource"></barChart>
	</div>
</template>
<script>
	import barChart from '@/components/charts/barChart.vue'
	export default {
	  name: '',
	  components: { barChart },
	  data(){
	  	return {
	       dataSource: {
              // Chart Configuration
              chart: {
                  caption: "Countries With Most Oil Reserves [2017-18]",
                  subCaption: "In MMbbl = One Million barrels",
                  xAxisName: "Country",
                  yAxisName: "Reserves (MMbbl)",
                  numberSuffix: "K",
                  theme: "fusion",
              },
              // Chart Data
              data: [
                {
                    label: "Venezuela",
                    value: 90
                }, {
                    label: "Saudi",
                    value: 260
                }, {
                    label: "Canada",
                    value: 180
                }, {
                    label: "Iran",
                    value: 140
                }, {
                    label: "Russia",
                    value: 115
                }, {
                    label: "UAE",
                    value: 100
                }, {
                    label: "US",
                    value: 30
                }, {
                    label: "China",
                    value: 30
                }
              ]
          }
	  	}
	  },
	  mounted () {
	    
	  }
	}
</script>
<style scoped>
.home {
	position: relative;
	height: 100vh;
}
</style>
<style>

</style>
