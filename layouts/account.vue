<template>
  <div class="h-full">
    <Navbar />
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
import Navbar from '~/components/Navbar.vue'
@Component({
  components: {
    Menu,
    Navbar
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
