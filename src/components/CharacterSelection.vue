<template>
    <div class='container'>
        <ScrollableList class="list">
            <CharacterTile charClass="deception" />
            <CharacterTile charClass="arcane" />
            <CharacterTile charClass="devotion" />
            <CharacterTile charClass="martial" />
            <CharacterTile charClass="deception" />
            <CharacterTile charClass="deception" />
            <CharacterTile charClass="deception" />
            <CharacterTile charClass="deception" />
            <CharacterTile charClass="deception" />
            <CharacterTile charClass="deception" />
            <CharacterTile charClass="deception" />
        </ScrollableList>
        <b-button class='create'>Create</b-button>
    </div>
</template>
<script lang="ts">
import Vue from "vue";
import CharacterTile from './CharacterTile.vue';
import ScrollableList from './ScrollableList.vue';
export default Vue.extend({
  name: "CharacterSelection",
  props: {
    msg: String
  },
  components: {
      CharacterTile,
      ScrollableList
  }
});
</script>
<style scoped>
    .container {
        height: 100%;
        display: flex;
        flex-direction: column;
    }
    .list {
        flex-grow: 1;
        display: flex;
    }
</style>

