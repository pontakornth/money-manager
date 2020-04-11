<template>
  <div class="padded">
    <h1 class="title is-1">สถิติ</h1>
    <div class="columns is-multiline">
      <div class="column is-half">
        <h2 class="title is-2 has-text-centered">ข้อมูลรายจ่าย</h2>
        <DonutChart :chart-data="expenseData" />
      </div>
      <div class="column is-half">
        <h2 class="title is-2 has-text-centered">ข้อมูลรายรับ</h2>
        <DonutChart :chart-data="incomeData" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'
import DonutChart from '~/components/charts/DonutChart.vue'
@Component({
  layout: 'account',
  components: {
    DonutChart
  }
})
class Chart extends Vue {
  expenseData = {
    labels: ['อาหาร', 'การศึกษา', 'บันเทิง'],
    datasets: [
      {
        labels: '# Money spended',
        data: [200, 500, 200],
        backgroundColor: [
          'rgb(255, 99, 132)',
          'rgb(54, 162, 235)',
          'rgb(255, 206, 86)'
        ]
      }
    ]
  }

  incomeData = {
    labels: ['ค่าขนม', 'ค่าจ้าง', 'ของขวัญ'],
    datasets: [
      {
        labels: '# Money Recieved',
        data: [1500, 2500, 200],
        backgroundColor: [
          'rgb(255, 99, 132)',
          'rgb(54, 162, 235)',
          'rgb(255, 206, 86)'
        ]
      }
    ]
  }
}
export default Chart
</script>

<style lang="scss" scoped>
.ledger-form {
  width: 50%;
}
.padded {
  padding: 1rem;
}
.mt-1 {
  margin-top: 1rem;
}
</style>
