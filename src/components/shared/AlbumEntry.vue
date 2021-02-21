<template>
    <div class="album-entry-container">
        <div class="image-placeholder" />
        <div class="artist-album">{{album.artistName}} - {{album.albumName}}</div>
        <div class="album-info">{{album.songCount}} songs, {{album.totalTime}}</div>
        <Icon v-if="buttonType=='remove'" :icon="icons.remove" class="svg-button" />
        <Icon v-else :icon="icons.options" class="svg-button"/>
    </div>
</template>

<script>
import { Icon } from '@iconify/vue';
import roundRemove from '@iconify/icons-ic/round-remove';
//import roundShuffle from '@iconify/icons-ic/round-shuffle';
import roundMoreHoriz from '@iconify/icons-ic/round-more-horiz';

export default {
    components: {
        Icon,
    },
    props: {
        buttonType: {
            type: String,
            validator(value) {
                return ["remove", "options"].includes(value);
            }
        },
        album: {
            type: Object,
            default() {
                return {
                    albumName: "Album",
                    artistName: "Artist",
                    songCount: "10",
                    totalTime: "60:13"
                };
            },
        },
    },
    data() {
        return {
            icons: {
                remove: roundRemove,
                options: roundMoreHoriz
            },
        };
    },
}
</script>

<style scoped>
    .album-entry-container {
        position: relative;
        height: 6.5rem;
        left: 0;
        right: 0;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .image-placeholder {
        width:4.5rem;
        height:4.5rem;
        margin-left: 1rem;
        background-color: var(--light-colour);
        flex-shrink: 0;
    }
    .svg-button {
        font-size: 4.5rem;
        margin-right: 1rem;
    }

    .artist-album {
        position: absolute;
        top: 1.7rem;
        left: 6.4rem;
        font-size: 1.4rem;
    }

    .album-info {
        position: absolute;
        bottom: 1.5rem;
        left: 6.5rem;
        font-size: 1rem;
    }

</style>