<template>
      <v-footer
        :fixed="fixed"
        app
      >
        <v-card
          class="mx-auto"
          flat
        >
          {{ new Date().getFullYear() }} ::
          <a
            :href="devurl"
            target="_blank"
            >
            <strong>SoL Dog Media</strong>
          </a>
        </v-card>
      </v-footer>
</template>

<script>
    export default {
      name: "Footer",
      data () {
        return {
          fixed: true,
          devurl: "https://soldogmedia.ca"
        }
      },
    };
</script>
