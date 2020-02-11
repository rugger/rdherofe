<template>
  <nuxt />
</template>

<script>
  import Footer from '../components/Footer/Footer'
  export default {
    name: 'landing',
    title: 'RD Hero :: Home',
    components: { Footer }
  }
</script>

<style scoped>
  .radio-hero-image {
    background-color: #DADADA;
    background-image: url('../assets/images/onairmic.jpg');
    background-repeat: no-repeat;
    background-position: center;
    height: 750px;
    background-size: cover;
    position: relative;
  }
  .radio-hero-text {
    color: ghostwhite;
  }
</style>

