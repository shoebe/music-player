<template>
    <div>
        <div class="image-slider-container">
            <div class="image-placeholder"/>
            <input type="range" min="0" max="180" step="any" value="0" class="time-slider">
        </div>
        <div class="song-name">Song name</div>
        <div class="artist-album-name">Artist - Album</div>
        <div class="time-info">1:30 / 3:30</div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    .image-slider-container {
        display: flex;
        align-items: center;
    }
    .image-placeholder {
        width:4.5rem;
        height:4.5rem;
        background-color: var(--light-colour);
        flex-shrink: 0;
    }
    .time-slider {
        flex-grow: 1;
        margin-left: 1.2rem;
        margin-right: 1.2rem;
        outline: none;
        appearance: none;
        height: 0rem;
        border: 0.35rem solid var(--light-colour);
        background-color: var(--light-colour);
        border-radius: 0.35rem;
    }
    .time-slider::-webkit-slider-thumb {
        border: 0.85rem solid var(--light-colour);
        border-radius: 1.5rem;
        background-color: var(--light-colour);
        box-shadow: 0 0 0.2rem 0.2rem var(--dark-shadow-colour);
        height:0;
        width:0;
    }
    .time-slider::-moz-range-thumb {
        border: 0.85rem solid var(--light-colour);
        border-radius: 1.5rem;
        background-color: var(--light-colour);
        box-shadow: 0 0 0.2rem 0.2rem var(--dark-shadow-colour);
        height:0;
        width:0;
    }
    .time-slider::-ms-thumb {
        border: 0.85rem solid var(--light-colour);
        border-radius: 1.5rem;
        background-color: var(--light-colour);
        box-shadow: 0 0 0.4rem 0.4rem var(--dark-shadow-colour);
        height:0;
        width:0;
    }
    .song-name {
        position: absolute;
        top: 0;
        left: 5.5rem;
        font-size: 1.3rem;
    }
    .artist-album-name {
        position: absolute;
        left:5.5rem;
        bottom: -0.1rem;
        font-size:1.1rem;
    }

    .time-info {
        position: absolute;
        font-size:1rem;
        right:1.2rem;
        top:0.5rem;
    }
</style>