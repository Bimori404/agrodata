<template>
  <div class="content">
    <div class="md-layout">
      <!-- Contenido -->
      <!-- 
        Colores de las graficas
          
          Temperatura                         -> orange
          Precipitacion                       -> blue
          Humedad Realativa                   -> green
          Velocidad y direccion del viento    -> gray
          Radiacion Solar                     -> red

          - data-background-color="orange"
          - data-background-color="blue"
          - data-background-color="green"
          - data-background-color="gray"
          - data-background-color="red"

      -->
      <div class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-33">
        <chart-card :chart-data="dailyDataLog2.data" :chart-options="dailyDataLog2.options"
          :chart-type="'Line'" data-background-color="orange">

          <template slot="content">
            <h4 class="title">Temperatura</h4>
            <!-- -->
          </template>

          <template slot="footer">
            <!-- -->
          </template>
        </chart-card>
      </div>
      <!----------------------------------------------------------------------->
      <div class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-33">
        <chart-card :chart-data="dailyDataLog.data" :chart-options="dailyDataLog.options"
          :chart-type="'Line'" data-background-color="blue">
          <template slot="content">
            <h4 class="title">Precipitacion</h4>
            <!--  -->
          </template>

          <template slot="footer">
            <!-- -->
          </template>
        </chart-card>
      </div>
      <!----------------------------------------------------------------------->
      <div class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-33">
        <chart-card :chart-data="dailyDataLog.data" :chart-options="dailyDataLog.options"
          :chart-type="'Line'" data-background-color="green">
          <template slot="content">
            <h4 class="title">Humedad relativa</h4>
            <!-- -->
          </template>

          <template slot="footer">
            <!-- -->
          </template>
        </chart-card>
      </div>
      <!----------------------------------------------------------------------->
      <div class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-50">
        <chart-card :chart-data="dailyDataLog3.data" :chart-options="dailyDataLog3.options"
          :chart-type="'Line'" data-background-color="gray">
          <template slot="content">
            <h4 class="title">Velocidad y direccion del viento</h4>
            <!-- -->
          </template>

          <template slot="footer">
            <!-- -->
          </template>
        </chart-card>
      </div>
      <!----------------------------------------------------------------------->
      <div class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-50">
        <chart-card :chart-data="dailyDataLog2.data" :chart-options="dailyDataLog2.options"
          :chart-type="'Line'" data-background-color="red">
          <template slot="content">
            <h4 class="title">Radiacion solar</h4>
            <!-- -->
          </template>

          <template slot="footer">
            <!-- -->
          </template>
        </chart-card>
      </div>
    </div>
  </div>
</template>

<script>
import {
  // StatsCard,
  ChartCard,
  // NavTabsCard,
  // NavTabsTable,
  // OrderedTable,
} from "@/components";

export default {
  components: {
    // StatsCard,
    ChartCard,
    // NavTabsCard,
    // NavTabsTable,
    // OrderedTable,
  },

  // Info que se muestra en el contenido //
  data() {
    return {
      dailyDataLog: {
        data: {
          labels: ["00", "03", "06", "09", "12", "15", "18", "21"],
          series: [[12, 17, 7, 17, 23, 18, 38, 22]],
        },
        options: {
          lineSmooth: this.$Chartist.Interpolation.cardinal({
            tension: 0,
          }),
          low: 0,
          high: 50,
          chartPadding: {
            top: 0,
            right: 0,
            bottom: 0,
            left: 0,
          },
        },
      },
      dailyDataLog2: {
        data: {
          labels: ["00", "03", "06", "09", "12", "15", "18", "21"],
          series: [[12, 17, 7, 17, 23, 18, 38, 22]],
        },

        options: {
          lineSmooth: this.$Chartist.Interpolation.cardinal({
            tension: 0,
          }),
          low: 0,
          high: 50,
          chartPadding: {
            top: 0,
            right: 0,
            bottom: 0,
            left: 0,
          },
        },
      },
      dailyDataLog3: {
        data: {
          labels: ["00", "03", "06", "09", "12", "15", "18", "21"],
          series: [[12, 17, 7, 17, 23, 18, 38, 42]],
        },

        options: {
          lineSmooth: this.$Chartist.Interpolation.cardinal({
            tension: 0,
          }),
          low: 0,
          high: 50,
          chartPadding: {
            top: 0,
            right: 0,
            bottom: 0,
            left: 0,
          },
        },
      },
    };
  },
};
</script>
