<template>
    <div class="list-item" >
        <img class="icon" :src="this.classes[this.charClass]" />
        <div>
            <p>Character</p>
            <p>Level 3</p>
        </div>
    </div>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    name: 'CharacterTile',
    props: {
        charClass: String
    },
    data() {
        return {
            classes: {
                deception: "/classicons/deception.png",
                arcane: "/classicons/arcane.png",
                devotion: "/classicons/devotion.png",
                martial: "/classicons/martial.png"
            }
        };
    }
})
</script>
<style scoped>
    @media(orientation: landscape) {        
        .list-item {
            padding: 10px;
            width: 30%;
            max-width: 200px;
            height: 50%;
            max-height: 100px;
        }
    }

    @media(orientation: portrait) {
        .list-item {
            padding: 10px;
            height: 15%;
        }
    }

    .list-item {
        display: grid;
        grid-template-columns: 25% auto;
    }

    .icon {
        max-height: 100%;
        max-width: 100%;
        align-self: center;
        object-fit: contain;
    }
</style>
