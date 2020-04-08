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
            <a class="button is-light">
              เข้าสู่ระบบ
            </a>
          </div>
        </b-navbar-item>
      </template>
    </b-navbar>

    <section class="main-content columns">
      <aside class="column is-2 section">
        <p class="menu-label is-hidden-touch">
          General
        </p>
        <ul class="menu-list">
          <li v-for="(item, key) of items" :key="key">
            <nuxt-link :to="item.to" exact-active-class="is-active">
              <b-icon :icon="item.icon" /> {{ item.title }}
            </nuxt-link>
          </li>
        </ul>
      </aside>

      <div class="container column is-10">
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
