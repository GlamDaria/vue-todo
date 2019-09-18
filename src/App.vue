<template>
  <div class="container">
      <h1 class="mt-3">Create Your Own Playlist!</h1>
      <app-actions v-on:sendSongToTheApp="addSongToTheArray($event)"></app-actions>
      <app-display v-bind:displaySongs="songs"></app-display>
  </div>
</template>

<script>
import Action from './components/Actions';
import Display from './components/Display';
export default {
  data(){
    return{
      songs : [{
        name: "Superpower",
        singer: "Adam Lambert"
      },
      {
        name: "New Eyes",
        singer: "Adam Lambert"
      },
      {
        name: "Comin' in hot",
        singer: "Adam Lambert"
      }]
    }
  },
  components:{
    appActions : Action,
    appDisplay : Display
  },
  methods:{
    addSongToTheArray(song){
      this.songs.push(song);
    }
  }
}
</script>

<style>

</style>
