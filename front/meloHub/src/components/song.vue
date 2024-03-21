<template>
    <div class="song" @click="play" @mouseover="setHover(true)" @mouseleave="setHover(false)">
      <audio ref="audioElement" controls class="song__audio" @loadedmetadata="getDuration">
        <source class="song__src" :src="audio" type="audio/mpeg">
      </audio>
      <div class="song__info">
        <p class="song__number">{{ number }}.</p>
        <div class="song__cover">
          <img :src="cover" :alt="cover" class="song__cover-img">
        </div>
        <p class="song__title">{{ title }}</p>
        <p class="song__author">{{ author }}</p>
      </div>
      <div class="song__actions">
        <div class="song__addendum" :class="{ 'hovered': isHovered }">
            <Addendum :duration="duration" />
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import Addendum from './Addendum.vue';
  
  export default {
    components: {
      Addendum
    },
    props: {
      number: {
        type: Number
      },
      cover: {
        type: String
      },
      title: {
        type: String
      },
      author: {
        type: String
      },
      audio: {
        type: String
      }
    },
    methods: {
      play() {
        this.$refs.audioElement.play();
      },
      getDuration() {
        const audioEl = this.$refs.audioElement;
        const durationAudio = Math.floor(audioEl.duration);
  
        const min = Math.floor(durationAudio / 60);
        const sec = Math.floor(durationAudio % 60);
  
        this.duration = `${min}:${sec < 10 ? '0' : ''}${sec}`;
      },
      setHover(value) {
        this.isHovered = value;
      }
    },
    data() {
      return {
        duration: '0:00',
        isHovered: false
      };
    }
  };
  </script>
  

<style lang="scss">

.song {
    position: relative;

    display: flex;
    align-items: center;
    justify-content: space-between;

    padding: 5px 10px;

    transition: .1s;

    &:hover {
        background-color: #5c8374;
        opacity: .5;

        border-radius: 10px;
    }

    &__audio {
        display: none;
    }

    &__info {
        display: flex;
        align-items: center;
    }

    &__number {
        opacity: .7;
        margin-right: 15px;
    }

    &__cover {
        width: 30px;
        height: 30px;   

        margin-right: 15px;
    }

    &__title {
        width: 200px;
        margin-right: 15px;
    }
}
</style>