<template>
  <div>
    <h1 class="title is-1">บัญชีรายรับรายจ่าย</h1>
    <form class="ledger-form">
      <b-field label="รายการ">
        <b-input type="text" name="title" placeholder="กะเพราหมูสับ" />
      </b-field>
      <div class="columns is-gapless">
        <div class="column is-4">
          <b-field label="ประเภท">
            <b-select>
              <option value="income">รายรับ</option>
              <option value="income">รายจ่าย</option>
            </b-select>
          </b-field>
        </div>
        <div class="column is-4">
          <b-field label="ประเภทรายการ">
            <b-select>
              <option value="อาหาร">อาหาร</option>
              <option value="เครื่องแต่งกาย">เครื่องแต่งกาย</option>
              <option value="การศึกษา">การศึกษา</option>
            </b-select>
          </b-field>
        </div>
        <div class="column is-4">
          <b-field label="จำนวนเงิน">
            <b-input type="number" step="0.01" />
          </b-field>
        </div>
      </div>
    </form>
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

<style lang="scss" scoped>
.ledger-form {
  width: 50%;
}
</style>
