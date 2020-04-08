<template>
  <section class="section">
    <div class="columns is-centered is-mobile">
      <div class="column forms is-12-mobile is-6-tablet is-4-desktop">
        <h1 class="title is-1">Money Manager</h1>
        <b-field class="f-label" label="อีเมล">
          <b-input class="f-input" type="email" name="email" />
        </b-field>
        <b-field class="f-label" label="รหัสผ่าน">
          <b-input
            class="f-input"
            type="password"
            name="password"
            maxlength="30"
          />
        </b-field>
        <div class="buttons">
          <b-button class="f-input" type="is-success">เข้าสู่ระบบ</b-button>
          <b-button class="f-input" type="is-danger" outlined
            >ลืมรหัสผ่าน</b-button
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// import Card from '~/components/Card'
import { Vue, Component } from 'nuxt-property-decorator'

@Component
class Login extends Vue {}
export default Login
</script>
