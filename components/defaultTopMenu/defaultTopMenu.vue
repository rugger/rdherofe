<template>
    <div class="defaultTopMenu">
      <v-app-bar
        color="orange darken-3"
        dense
        dark
        :clipped-left="leftClipped"
        :clipped-right="rightClipped"
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
      <RDHeroAppDrawer appDrawer="appDrawer" v-model="appDrawer" appGroup="appGroup"/>
      <v-navigation-drawer
        v-model="userDrawer"
        right
        app
        fixed
        :clipped = "userDrawerClipped"
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
  import RDHeroAppDrawer from '../RDHeroAppDrawer/RDHeroAppDrawer'
    export default {
      components: { RDHeroAppDrawer },
      name: 'defaultTopMenu',
        props: {
            appName: String,
        },
      data: () => ({
          appDrawer: false,
          userDrawer: false,
          userDrawerClipped: true,
          // appDrawerClipped: true,
          rightClipped: false,
          leftClipped: false,
          clipped: false,
        }),
      watch: {
        appGroup () {
          this.appDrawer = false
      },
      },
    };
</script>
