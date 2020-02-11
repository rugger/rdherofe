<template>
  <div class="musicscheduler">
    <v-row>
    <v-col
    cols9
    >
    <msToolBar />
    <MusicSchedulerTab />
    </v-col>
  </v-row>
  </div>
</template>

<script>
  import MusicSchedulerTab from '../components/MusicSchedulerTab/MusicSchedulerTab'
  import msToolBar from '../components/msToolBar/msToolBar'
  export default {
    props: { appName: String,
    },
    appName: 'Music Scheduler',
    name: 'musicscheduler',
    components: { msToolBar, MusicSchedulerTab },
    layout: 'musicsched/musicsched',
    schedOpen: false,
    clipped: false,
  }
</script>

<style scoped>

</style>
