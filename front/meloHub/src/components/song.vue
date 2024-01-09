<template>
    <div class="song">
        <div class="song__info">
            <p class="song__number">
                {{ number }}
            </p>

            <div class="song__cover">
                <img :src="cover" :alt="cover" class="song__cover-img">
            </div>

            <p class="song__name">
                {{ title }}
            </p>

            <p class="song__author">
                {{ author }}
            </p>
        </div>
        <div class="song__actions">
            <div class="song__addendum">
                
            </div>
        </div>
    </div>
</template>

<script>
export default {
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
        }
    }    
}
</script>

<style lang="scss">
    
</style>