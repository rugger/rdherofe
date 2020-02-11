<template>
    <v-app light>
      <v-content class="radio-hero-image">
        <v-container>
          <nuxt />
        </v-container>
      </v-content>
    <Footer />
    </v-app>
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
</style>
