<template>
<!--     <v-col no-gutters> -->
       <v-col
         style="margin-right: 10%"
         cols="5"
         class="float-right"
         >
        <LandingLogin  class="float-right pt-12 pr-10"/>
     </v-col>
</template>

<script>
  import LandingLogin from '../components/LandingLogin/LandingLogin'
  export default {
    name: 'home',
    title: 'Home :: RD Hero',
    layout: 'landing',
    components: { LandingLogin },
    data () {
      return {

      }
    },
    head () {
      return {
        title: this.title,
        meta: [
          // hid is used as unique identifier. Do not use `vmid` for it as it will not work
          { hid: 'description', name: 'description', content: 'A Suite of Helper Apps for Rivendell Audio' }
        ]
      }
    }
  }
</script>

<style scoped>

</style>
