<template>
  <div class="card">
    <header class="card-header">
      <p class="card-header-title">
        {{ title }}
      </p>
    </header>
    <div class="card-content">
      <div class="content">
        <p>ราคา: {{ price }}</p>
        <p>เก็บเงินไว้ : {{ current }}</p>
        <p>เหลือ : {{ left }}</p>
      </div>
      <div class="buttons">
        <b-button type="is-success">เพิ่มเงิน</b-button>
        <b-button type="is-warning">ถอนเงิน</b-button>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'nuxt-property-decorator'
@Component
class BudgetCard extends Vue {
  @Prop({ type: String }) title!: string
  @Prop({ type: Number }) price!: number
  @Prop({ type: Number }) current!: number
  get left() {
    return this.price - this.current
  }
}
export default BudgetCard
</script>
