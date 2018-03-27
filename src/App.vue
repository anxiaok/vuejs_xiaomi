<template>
  <div id="app">
    <Header />
    <router-view/>
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header'
import Footer from '@/components/Footer'
import 'animate.css'
export default {
  name: 'App',
  components:{
    Header,Footer
  }
}
</script>

<style>

</style>
