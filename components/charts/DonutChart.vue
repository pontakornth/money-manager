<script lang="ts">
import { Doughnut, mixins } from 'vue-chartjs'
import { Component, Vue, Prop } from 'nuxt-property-decorator'
const { reactiveProp } = mixins
@Component({
  extends: Doughnut,
  mixins: [reactiveProp]
})
class DonutChart extends Vue {
  public renderChart!: (chartData: any, options: any) => void
  @Prop({ type: Object }) chartData!: any
  @Prop({ type: Object }) options!: any
  mounted() {
    this.renderChart(this.chartData, this.options)
  }
}
export default DonutChart
</script>
