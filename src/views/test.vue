import Vue from 'vue';
import VueFusionCharts from 'vue-fusioncharts';
import FusionCharts from 'fusioncharts';
import Column2D from 'fusioncharts/fusioncharts.charts';
import FusionTheme from 'fusioncharts/themes/fusioncharts.theme.fusion';

Vue.use(VueFusionCharts, FusionCharts, Column2D, FusionTheme);
export default {
name: 'app',
data() {
return {
"type": "column2d",
"renderAt": "chart-container",
"width": "550",
"height": "350",
"dataFormat": "json",
"datasource": {
"chart": {
"caption": "Number of visitors in the last 3 days",
"subCaption": "Bakersfield Central vs Los Angeles Topanga",
"theme": "fusion"
},
"data": [{
"label": "Mon",
"value": "15123"
}, {
"label": "Tue",
"value": "14233"
}, {
"label": "Wed",
"value": "25507"
}]
}
}
}
}

<template>
<div id="app">
<div id="chart-container">
<fusioncharts
:type="type"
:width="width"
:height="height"
:dataformat="dataformat"
:datasource="datasource"
>
</fusioncharts>
</div>
</div>
</template>