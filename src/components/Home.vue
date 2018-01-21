<template>
  <div>
    <Navbar/>
    <LandingPage/>
    <Footer/>
  </div>
</template>

<script>
import Navbar from './Navbar'
import LandingPage from './LandingPage'
import Footer from './Footer'

export default {
  components: {
    Navbar,
    LandingPage,
    Footer
  }
}
</script>

<style lang="scss">
</style>
