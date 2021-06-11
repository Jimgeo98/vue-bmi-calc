<template>
  <Header />
  <Bmi />
  <Stats />
  <Footer />

</template>

<script>
import Bmi from './components/Bmi.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Stats from './components/Stats.vue'

export default {
  name: 'App',
  components: {
    Bmi,
    Header,
    Footer,
    Stats
  }
}
</script>
