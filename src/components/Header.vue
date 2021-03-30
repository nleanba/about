<template>
  <header>
    <div class="left">
      <img alt="nleanba logo" src="../assets/logo.png">
    </div>
    <div class="right">
      <svg viewBox="0 0 64.38 19">
        <text x="0" y="15">nleanba</text>
      </svg>
    </div>
  </header>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({})
export default class HeaderBar extends Vue {}
</script>

<style lang="scss" scoped>
@use '../vars';

header {
  height: 16rem;
  display: flex;
  max-width: 100%;
}

.left {
  flex: 0 1 16rem;
  display: flex;
  flex-direction: column;
  justify-content: center;

  & img {
    margin: 0 auto;
    width: 100%;
  }
}

.right {
  background-color: vars.$c_10;
  flex: 1;
  // line-height: 8rem;
  padding: min(4rem, 5vw);
  font-weight: 800;

  svg {
    min-width: 50vw;
    width: 100%;
    height: calc(16rem - 2 * min(4rem, 5vw));
  }
}
</style>
