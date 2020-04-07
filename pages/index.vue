<template>
  <section class="section">
    <div class="columns is-mobile">
      <card title="Free" icon="piggy-bank">
        Managing money easy way
      </card>

      <card title="Responsive" icon="book">
        Easy planning
      </card>

      <card title="Modern" pack="mdi" icon="shield-account">
        Care about your security
      </card>

      <card title="Lightweight" icon="heart">
        Built with love
      </card>
    </div>
  </section>
</template>

<script>
import Card from '~/components/Card'

export default {
  name: 'HomePage',

  components: {
    Card
  }
}
</script>
