<template>
    <div class="playlist-container">
        <AlbumEntry :buttonType="remove" />
    </div>
</template>

<script>
import AlbumEntry from "../shared/AlbumEntry.vue"
export default {
    components: {
        AlbumEntry
    }
}
</script>

<style scoped>
    .playlist-container {
        position:absolute;
        left: 0;
        right: 0;
        top: 0;
        height: 100%;
        display: flex;
        flex-direction: column;
        background-color: var(--bg-colour);
    }
</style>