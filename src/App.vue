<template>
  <div id="app">
    <CharacterSelection/>
  </div>
</template>

<script lang='ts'>
import Vue from 'vue';
import VueMeta from 'vue-meta';
import VueBootstrap from 'bootstrap-vue';
import CharacterSelection from './components/CharacterSelection.vue';
// import Shell from './components/Shell.vue';

Vue.use(VueMeta);
Vue.use(VueBootstrap);

export default Vue.extend({
  name: 'app',
  components: {
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
  }
});
</script>

<style>
#app, body, html {
  height: 100%;
}
</style>
