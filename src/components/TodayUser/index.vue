<template>
  <common-card title="今日交易量" :value="orderUser">
    <template>
      <v-chart :options="getOption()" />
    </template>
    <template v-slot:footer>
      <span>退货率 </span>
      <span class="emphasis">{{ returnRate }}</span>
    </template>
  </common-card>
</template>

<script>
import commonCardMixin from '../../mixins/commonCardMixin'
import commonDataMixin from '../../mixins/commonDataMixin'
export default {
  mixins: [commonCardMixin, commonDataMixin],
  methods: {
    getOption() {
      return {
        color: ['#3398db'],
        tooltip: {},
        series: [
          {
            type: 'bar',
            name: '用户实时交易量',
            data: this.orderUserTrend,
            barWidth: '60%'
          }
        ],
        xAxis: {
          type: 'category',
          data: this.orderUserTrendAxis,
          show: false
        },
        yAxis: {
          show: false
        },
        grid: {
          top: 0,
          left: 0,
          bottom: 0,
          right: 0
        }
      }
    }
  }
}
</script>

<style></style>
