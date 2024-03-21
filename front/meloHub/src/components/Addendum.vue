<template>
    <div class="addendum">

        <div class="addendum__hover">
            <p>hi</p>
        </div>

        <img class="addendum__icon" :src="'/like_icon.svg'" alt="">

        <p class="addendum__duration">
            {{ duration }}
        </p>
    </div>
</template>
<script>
export default {
    props: {
        duration: {
            type: String
        }
    }
}
</script>
<style lang="scss">
.addendum {
    display: flex;
    align-items: center;
    gap: 20px;

    &__hover {
        display: none;
    }

    &__hover.hovered {
        display: block;
    }
}
</style>