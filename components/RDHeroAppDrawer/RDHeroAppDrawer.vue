<template>
    <div class="RDHeroAppDrawer">
      <v-navigation-drawer
        v-model="appDrawer"
        absolute
        temporary
        :clipped = "appDrawerClipped"
        app
      >
        <v-row color="teal" class="ml-2 mt-2">
          <v-btn icon @click.stop="appDrawer = !appDrawer">
            <v-icon>mdi-menu</v-icon>
          </v-btn>
          <h3 class="pl-3 mx-auto">Apps</h3>
        </v-row>
        <v-list
          nav
        >
          <v-list-item-group
            v-model="appGroup"
            active-class="orange--text text--darken-2"
          >
            <v-list-item
            href="musicscheduler"
            >
              <v-icon
                color="orange lighten-2"
              >mdi-calendar-clock</v-icon>
              <v-list-item-title>Music Scheduler</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-icon color="orange darken-2">mdi-traffic-light</v-icon>
              <v-list-item-title>Traffic Scheduler</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-icon color="orange lighten-1">mdi-microphone</v-icon>
              <v-list-item-title>Voice Tracker</v-list-item-title>
            </v-list-item>
            <v-list-item>
              <v-icon color="orange darken-1">mdi-library-music</v-icon>
              <v-list-item-title>Audio Library</v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </div>
</template>

<script>
    export default {
      name: 'RDHeroAppDrawer',
        props: {
          appDrawer: String,
          appName: String,
        },
      data () {
        return {
          appGroup: null,
          appDrawerClipper: true,
          appDrawer: false,
        }
      }
    };
</script>
