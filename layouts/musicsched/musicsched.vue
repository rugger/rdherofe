<template>
  <v-app light>
    <InfoBar />
    <defaultTopMenu appName="Music Scheduler"/>
    <v-content>
        <nuxt />
    </v-content>
<!--    <Footer />-->
  </v-app>
</template>

<script>
  import InfoBar from '../../components/InfoBar/InfoBar'
  import defaultTopMenu from '../../components/defaultTopMenu/defaultTopMenu'
  import Footer from '../../components/Footer/Footer'
  export default {
    props: {
      appName: String,
    },
    name: 'musicsched',
    title: 'Music Scheduler :: RD Hero',
    components: { InfoBar, defaultTopMenu, Footer }
  }
</script>
