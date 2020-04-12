<template>
  <div class="padded">
    <h1 class="title is-1">วางแผนการออม</h1>
    <div class="columns is-multiline">
      <div class="column is-4">
        <BudgetCard title="Nintendo Hub" :price="1200" :current="500" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'
import BudgetCard from '~/components/BudgetCard.vue'
@Component({
  layout: 'account',
  components: {
    BudgetCard
  }
})
class Planner extends Vue {}
export default Planner
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
