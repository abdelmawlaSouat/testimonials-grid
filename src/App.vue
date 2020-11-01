<template>
  <v-app>
    <v-main>
      <Testimonial/>
    </v-main>
  </v-app>
</template>

<script>
import Testimonial from './components/Testimonial'

export default {
  name: 'App',
  components: {
    Testimonial
  }
}
</script>
<style>
body {
  font-size: 13px;
}
</style>
