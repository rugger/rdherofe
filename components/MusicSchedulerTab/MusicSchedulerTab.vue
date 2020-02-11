<template>
  <div class="MusicSchedulerTab">
    <v-data-table
      v-model="selected"
      :headers="headers"
      :items="songs"
      :single-select='singleSelect'
      item-key="id"
      :show-select='showSelect'
      flat
      dense
    >
    </v-data-table>
  </div>
</template>

<script>
    export default {
      name: 'MusicSchedulerTab',
        props: {
        appName: String,
        },
      data () {
        return {
          singleSelect: false,
          showSelect: false,
          selected: [],
          headers: [
            { text: 'Cat', value: 'category'},
            { text: 'Group', value: 'group'},
            { text: 'ID', value: 'id'},
            { text: 'Song ID', value: 'sid'},
            { text: 'Title', value: 'title'},
            { text: 'Artist', value: 'artist'},
            { text: 'Album', value: 'album'},
          ],
          songs: [
            {
              category: 'AA',
              group: 'CanCon',
              id: 1234,
              sid: 10010,
              title: 'This is the Long Title',
              artist: 'Johnny B',
              album: 'My First One'
            },
            {
              category: 'AA',
              group: 'CanCon',
              id: 1434,
              sid: 10020,
              title: 'Short Title',
              artist: 'Clover Girl',
              album: 'Sings the Howls'
            },
          ]
          }
        }
      };
</script>
