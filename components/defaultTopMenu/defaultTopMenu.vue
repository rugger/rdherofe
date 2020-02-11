<template>
    <div class="MusicSchedTopMenu">
      <v-app-bar
        color="orange darken-3"
        dense
        dark
        :clipped-right="clipped"
        app
      >
        <v-app-bar-nav-icon @click.stop="appDrawer = !appDrawer"></v-app-bar-nav-icon>
        <v-toolbar-title> <slot name="appName">{{ appName }}</slot></v-toolbar-title>
          <v-spacer></v-spacer>
        <v-btn icon>
          <v-icon>mdi-calendar-check</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-cogs</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-help</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-bullhorn</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-bell</v-icon>
        </v-btn>
        <v-btn icon @click.stop="userDrawer = !userDrawer">
          <v-avatar size="30" color="teal">
            <span class="white--text font-weight-light" >JB</span>
          </v-avatar>
        </v-btn>
      </v-app-bar>
      <v-navigation-drawer
        v-model="appDrawer"
        absolute
        temporary
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
            <v-list-item>
              <v-icon color="orange lighten-2">mdi-calendar-clock</v-icon>
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

      <v-navigation-drawer
        v-model="userDrawer"
        right
        app
        fixed
        :clipped = "clipped"
      >
      <v-row
        class="ml-2"
        flat
      >
        <v-col
          cols="9"
        >
            <h3>My Account</h3>
          </v-col>
          <v-col
            cols="1"
          >
            <v-btn icon @click.stop="userDrawer = !userDrawer">
              <v-icon>mdi-close</v-icon>
            </v-btn>
          </v-col>
        </v-row>
        <v-card>
        </v-card>
      </v-navigation-drawer>
    </div>
</template>

<script>
    export default {
      name: 'MusicSchedTopMenu',
        props: {
            appName: String,
        },
      data: () => ({
          appDrawer: false,
          appGroup: null,
          userDrawer: false,
          clipped: true,
        }),
      watch: {
        appGroup () {
          this.appDrawer = false
      },
      },
    };
</script>
