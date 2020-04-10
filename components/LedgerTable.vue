<template>
  <b-table
    striped
    :mobile-cards="false"
    :data="transactions"
    :columns="columns"
  ></b-table>
</template>

<script lang="ts">
import { Vue, Component, Prop } from 'nuxt-property-decorator'
@Component
class LedgerTable extends Vue {
  @Prop({ type: Array }) transactions!: Array<any>
  columns = [
    {
      field: 'title',
      label: 'รายการ'
    },
    {
      field: 'income',
      label: 'รายรับ',
      numeric: true
    },
    {
      field: 'expense',
      label: 'รายจ่าย',
      numeric: true
    }
  ]
}
export default LedgerTable
</script>
