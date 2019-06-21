<template>
  <div id="app">
    <NavBar class="nav" />
    <!-- <div>test1</div> -->
    <!-- <div>test2</div> -->
    <div class="list">
      <CharacterSelection charClass="deception"/>
    </div>
    <!-- <CharacterSheet v-if="url.includes('sheet')" charClass="deception"/> -->
  </div>
</template>

<script lang='ts'>
/* eslint-disable */
import Vue from 'vue';
import VueMeta from 'vue-meta';
import VueBootstrap from 'bootstrap-vue';
import NavBar from './components/NavBar.vue';
import CharacterSelection from './components/CharacterSelection.vue';
import CharacterSheet from './components/CharacterSheet.vue';
// import Shell from './components/Shell.vue';

Vue.use(VueMeta);
Vue.use(VueBootstrap);

export default Vue.extend({
  name: 'app',
  components: {
    NavBar,
    CharacterSheet,
    CharacterSelection
  },
  metaInfo: {
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' }
    ],
    link: [
//      <link rel="manifest" href="/manifest.json">
      {rel: 'manifest', href: '/webappmanifest.json'}
    ]
  },
  data() {
    return {
      url: String
    }
  },
  mounted() {
    this.url = this.$el.baseURI;
  }
});
</script>

<style>
#app {
  height: 100vh;
}

#app {
  display: grid;
  grid-template-rows: 2rem calc(100% - 2rem);
}

.list {
  height: 100%;
}
</style>
