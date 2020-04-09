<template>
  <div class="h-full">
    <b-navbar type="is-primary">
      <template slot="brand">
        <b-navbar-item tag="nuxt-link" to="/">
          <b>Money Manager</b>
        </b-navbar-item>
      </template>
      <template slot="start">
        <b-navbar-item tag="nuxt-link" to="/">
          หน้าหลัก
        </b-navbar-item>
        <b-navbar-item href="#">
          วิธีการใช้งาน
        </b-navbar-item>
        <b-navbar-dropdown label="ตั้งค่า">
          <b-navbar-item href="#">
            บัญชี
          </b-navbar-item>
          <b-navbar-item href="#">
            ตั้งค่าอื่น ๆ
          </b-navbar-item>
        </b-navbar-dropdown>
      </template>

      <template slot="end">
        <b-navbar-item tag="div">
          <div class="buttons">
            <a class="button is-primary">
              <strong>สมัครสมาชิก</strong>
            </a>
            <nuxt-link to="/login" class="button is-light">
              เข้าสู่ระบบ
            </nuxt-link>
          </div>
        </b-navbar-item>
      </template>
    </b-navbar>

    <section class="columns h-full is-mobile">
      <div class="column is-2 has-background-light is-hidden-mobile">
        <Menu />
      </div>
      <div class="column is-12-mobile is-10-tablet">
        <div class="container gap-2">
          <nuxt />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { Vue, Component } from 'nuxt-property-decorator'
import Menu from '~/components/Menu.vue'
@Component({
  components: {
    Menu
  }
})
class Account extends Vue {}
export default Account
</script>

<style lang="scss">
.gap-2 {
  padding-top: 1rem;
  padding-bottom: 1rem;
}
</style>
