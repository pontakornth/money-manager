<template>
  <div>
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

    <section class="main-content columns">
      <div class="container column is-12">
        <nuxt />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        }
      ]
    }
  }
}
</script>
