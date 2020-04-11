<template>
  <b-menu class="p-3px has-background-light">
    <b-menu-list label="เมนู">
      <b-menu-item
        tag="nuxt-link"
        to="/ledger"
        icon="edit"
        pack="far"
        label="บัญชีรายรับรายจ่าย"
      />
      <b-menu-item icon="piggybank" label="วางแผนการออม" />
      <b-menu-item tag="nuxt-link" to="/chart" icon="piggybank" label="สถิติ" />
    </b-menu-list>
  </b-menu>
</template>

<style lang="scss" scoped>
.p-3px {
  padding: 0.5rem;
}
</style>
