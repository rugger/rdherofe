<template>
  <v-app>
    <defaultTopMenu />
    <v-content>
    <v-toolbar
      dense
      color="primary"
      dark
      extended
      extension-height="175"
      flat
    >
      <v-toolbar-title class="mx-auto" slot="extension">
        <span>Welcome to RD Hero</span>
        <h2>Being a Radio Hero starts Here!</h2>
        <v-layout row>
          <v-flex wrap>
            <v-btn icon>
              <v-avatar
                size="64"
                color="white"
              >
                <v-icon color="primary">mdi-music-note</v-icon>
              </v-avatar>
            </v-btn>
          </v-flex>
          <v-flex wrap>
            <v-btn icon>
              <v-avatar
                size="64"
                color="white"
              >
                <v-icon color="teal">mdi-car</v-icon>
              </v-avatar>
            </v-btn>
          </v-flex>
          <v-flex wrap>
            <v-btn icon>
              <v-avatar
                size="64"
                color="white"
              >
                <v-icon color="blue">mdi-traffic-stop</v-icon>
              </v-avatar>
            </v-btn>
          </v-flex>
          <v-flex wrap>
            <v-btn icon>
              <v-avatar
                size="64"
                color="white"
              >
                <v-icon color="purple">mdi-traffic-stop</v-icon>
              </v-avatar>
            </v-btn>
          </v-flex>
        </v-layout>
      </v-toolbar-title>
    </v-toolbar>
<!--    <v-content>-->
      <v-layout row>
        <v-flex xs12 md8 offset-md2>
          <v-card flat class="card--flex-toolbar" color="transparent">
            <v-container fluid grid-list-lg>
              <v-layout row wrap>
                <v-flex xs12>
                  <h2 class="white--text">Discover Vuebase</h2>
                </v-flex>
              </v-layout>
              <v-layout row wrap>
                <v-flex xs12 sm6 md6 lg4 v-for="item in links" :key="item.id">
                  <v-hover>
                    <v-card slot-scope="{ hover }" :class="`elevation-${hover ? 12 : 2}`">
                      <v-img
                        src=""
                        aspect-ratio="2.75"
                        height="125px"
                        :class="item.color"
                      ></v-img>

                      <v-card-title primary-title>
                        <div>
                          <h3 class="headline mb-0">{{item.title}}</h3>
                          <div>
                            {{item.description}}
                          </div>
                        </div>
                      </v-card-title>

                      <v-card-actions>
                        <v-btn text color="primary" class="learn-more-btn">
                          Learn more
                        </v-btn>
                        <v-spacer></v-spacer>
                        <v-btn text color="primary">Get started</v-btn>
                      </v-card-actions>
                    </v-card>
                  </v-hover>
                </v-flex>
              </v-layout>
            </v-container>
          </v-card>
        </v-flex>
      </v-layout>
  </v-content>
  </v-app>
</template>

<script>
import defaultTopMenu from '../components/defaultTopMenu/defaultTopMenu'
  export default {
    layout: 'blank/blank',
    title: 'Home :: RD Hero',
    components: { defaultTopMenu },
    data() {
      return {

        links: [
          {
            id: '1',
            title: 'Dashboard',
            description: 'Get detailed anlytics to measure and analyze how users engage with your app',
            color: 'orange'
          },
          {
            id: '2',
            title: 'Storage',
            description: 'Store and retrieve user-generated content, such as images, audio, and videos, without server-side code.',
            color: 'teal'
          },
          {
            id: '3',
            title: 'Notifications',
            description: 'Manage your notification campaigns and send messages to reach the right users at the right time',
            color: 'blue'
          },
          {
            id: '4',
            title: 'Authentification',
            description: 'Authenticate and manage users from a variety of providers without server-side-code',
            color: 'purple'
          }
        ],
      }
    }
  }
</script>

<style scoped>
  .outine-2 {
    border: 2px solid white;
  }
  .card--flex-toolbar {
    margin-top: -124px;
  }
  .learn-more-btn {
    text-transform: initial;
    text-decoration: underline;
  }
</style>
