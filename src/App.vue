<template>
  <ag-charts-vue :options="options"> </ag-charts-vue>
  <ag-charts-vue :options="options1"> </ag-charts-vue>
</template>

<script>

import { AgChartsVue } from 'ag-charts-vue3';

export default {
  name: 'App',
  components: {
    AgChartsVue
  },
  setup(){
    return{
      options: {
        // Data: Data to be displayed in the chart
        data: [
          {  avgTemp: 2.3 },
          {  avgTemp: 6.3},
          {  avgTemp: 16.2},
          {  avgTemp: 22.8 },
          {  avgTemp: 14.5 },
          {  avgTemp: 8.9},
        ],
        // Series: Defines which chart type and data to use
        series: [{ type: 'pie', angleKey: 'avgTemp', legendItemKey: 'avgTemp' }],
        legend:{
          position:'right',
          spacing:10
        }
      },
      options1: {
        // Data: Data to be displayed in the chart
        data: [
          {  avgTemp: 2.3 },
          {  avgTemp: 6.3},
          {  avgTemp: 16.2},
          {  avgTemp: 22.8 },
          {  avgTemp: 14.5 },
          {  avgTemp: 8.9},
        ],
        // Series: Defines which chart type and data to use
        series: [{ type: 'pie', angleKey: 'avgTemp', legendItemKey: 'avgTemp' }],
        legend:{
          position:'bottom',
          spacing:10
        }
      }
    }
  }
}
</script>
