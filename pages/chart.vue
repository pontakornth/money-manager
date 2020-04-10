<template>
  <div class="padded">
    <h1 class="title is-1">ข้อมูลการใช้เงิน</h1>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'

@Component({
  layout: 'account'
})
class Chart extends Vue {}
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
