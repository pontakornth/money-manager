<template>
  <div>
    <h1 class="title is-1">บัญชีรายรับรายจ่าย</h1>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'

@Component({
  layout: 'account'
})
class Ledger extends Vue {}
export default Ledger
</script>
