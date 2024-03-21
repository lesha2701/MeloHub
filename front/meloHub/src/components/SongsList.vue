<template>
  <div class="songsList">
    <ul class="songsList__items">
      <li v-for="song in songsList" :key="song.id" class="songsList__item">
        <Song 
          :number="songsList.indexOf(song) + 1"
          :cover="song.cover"
          :title="song.title"
          :author="song.author"
          :audio="song.audio"
        />
      </li>
    </ul>   
  </div>
</template>

<script>
import Song from './Song.vue';

export default {
    components: {
        Song
    },
    props: {
        songsList: {
            type: Array
        }
    }
}
</script>

<style lang="scss">
.songsList {
    background-color: #1b4242;
    padding: 10px 15px;

    border-radius: 20px;

    &__items {
        list-style: none;

        padding: 0;
    }
}
</style>