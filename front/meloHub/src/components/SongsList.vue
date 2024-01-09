<template>
    <div class="songsList">
        <Song 
            :number="1"
            :cover="'/papin_olimpos.png'"
            :title="'Зомби по имени Билли'"
            :author="'Папин Олимпос'"
        />
    </div>
</template>

<script>
import Song from './Song.vue';

export default {
    components: {
        Song
    }
}
</script>
<style lang="scss">
    
</style>