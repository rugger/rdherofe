<template>
    <div class="msToolBar">
      <v-toolbar
        color="grey lighten-4"
        dense
        flat
      >
        <v-btn icon>
          <v-icon color="green lighten-3">mdi-music-note</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon color="blue lighten-3">mdi-clock</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon color="yellow darken-2">mdi-shield-sun</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon color="red lighten 3">mdi-calendar</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon color="teal lighten-2">mdi-update</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon color="orange lighten-2">mdi-chart-scatter-plot</v-icon>
        </v-btn>
      </v-toolbar>
    </div>
</template>

<script>
    export default {
      name: 'msTooBar',
        props: {
        },
    };
</script>
