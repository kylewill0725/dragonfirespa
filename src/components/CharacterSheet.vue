<template>
    <div class="container">
        <img :src="this.classes[this.charClass]" />
        <span>Character</span>
        <span>Half-ogre Rogue</span>
    </div>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    name: 'CharacterSheet',
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
        }
    }
})
</script>
<style scoped>
    .container {
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    
    img {
        object-fit: contain;
    }
</style>

