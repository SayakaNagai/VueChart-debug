<template>
  <v-content>
    <v-container>
      <!-- chartData に代入をしている -->
      <v-row>
        <v-col :cols="3">
          <MainChart
            class="chart"
            :option="{ maintainAspectRatio: false }"
            :chart-data="chartData"
            :width="100"
            :height="100"
          />
        </v-col>
      </v-row>
    </v-container>
  </v-content>
</template>

<script>
import MainChart from '@/components/BarChart'
export default {
  components: {
    MainChart
  },
  data() {
    return {
      chartData: {
        labels: ['January', 'February', 'March', 'April', 'May'],
        datasets: [
          {
            label: 'Sample1',
            data: [28, 20, 30, 40, 50],
            backgroundColor: [
              'rgba(255, 99, 132, 0.2)',
              'rgba(54, 162, 235, 0.2)',
              'rgba(255, 206, 86, 0.2)',
              'rgba(75, 192, 192, 0.2)',
              'rgba(153, 102, 255, 0.2)',
              'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
              'rgba(255, 99, 132, 1)',
              'rgba(54, 162, 235, 1)',
              'rgba(255, 206, 86, 1)',
              'rgba(75, 192, 192, 1)',
              'rgba(153, 102, 255, 1)',
              'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
          }
        ]
      }
    }
  }
}
</script>

<style>
.v-content {
  max-width: 20% !important;
}
</style>
