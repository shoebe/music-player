<template>
    <div class="base-container">
        <div class="song-control-container"> 
            <Icon :icon="icons.previous" class="svg-button skip"/>
            <Icon :icon="icons.pause" class="svg-button playpause"/>
            <Icon :icon="icons.next" class="svg-button skip"/>
        </div>
        <TheSongInfo class="song-info" />
        <Icon v-if="expanded" @click="expand" :icon="icons.retract" class="svg-button expand-retract" />
        <Icon v-else @click="expand" :icon="icons.expand" class="svg-button expand-retract" />
    </div>

</template>

<script>
import { Icon } from '@iconify/vue';

import roundExpandMore from '@iconify/icons-ic/round-expand-more';
import roundExpandLess from '@iconify/icons-ic/round-expand-less';

import roundPlayArrow from '@iconify/icons-ic/round-play-arrow';
import roundPause from '@iconify/icons-ic/round-pause';
import roundFastForward from '@iconify/icons-ic/round-fast-forward';
import roundFastRewind from '@iconify/icons-ic/round-fast-rewind';

import TheSongInfo from "./TheSongInfo.vue"

// import roundRemove from '@iconify/icons-ic/round-remove';
// import roundShuffle from '@iconify/icons-ic/round-shuffle';
// import roundMoreHoriz from '@iconify/icons-ic/round-more-horiz';


export default {
    components: {
        Icon,
        TheSongInfo,
    },
    data() {
        return {
            icons: {
                play: roundPlayArrow,
                pause: roundPause,
                next: roundFastForward,
                previous: roundFastRewind,
                retract: roundExpandMore,
                expand: roundExpandLess,
            },
            playing: false,
            expanded: false,
        };
    },
    methods: {
        expand() {
            this.expanded = !this.expanded;
        }
    },
};
</script>

<style scoped>
    .base-container {
        position: absolute;
        background-color: var(--bg-colour);
        box-shadow: 0 0 0.4rem 0.4rem var(--dark-shadow-colour);
        border-radius: 0.4rem;
        height: 6.5rem;
        left: 0%;
        right: 0%;
        bottom: 0;
        display: flex;
        align-items: center;
    }
    .song-control-container {
        width: min-content;
        display: flex;
        align-items: center;
        margin-right: 1.2rem;
        margin-left: 1.2rem;
    }
    .svg-button {
        color: var(--light-colour);
    }
    .skip {
        font-size: 3.5rem;
    }
    .playpause {
        font-size: 4.5rem;
    }
    .song-info {
        position: relative;
        flex-grow: 1; /* should take up all leftover space */
    }
    .expand-retract {
        font-size: 6.5rem;
    }

</style>