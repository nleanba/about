<template>
  <div id="app">
    <HeaderBar />
    <Main />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Main from './components/Main.vue';
import HeaderBar from './components/Header.vue';

@Component({
  components: {
    HeaderBar,
    Main,
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import url('https://rsms.me/inter/inter.css');

:root { font-family: 'Inter', sans-serif; }
@supports (font-variation-settings: normal) {
  :root { font-family: 'Inter var', sans-serif; }
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
}
</style>
