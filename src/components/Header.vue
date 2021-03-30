<template>
  <header>
    <div class="left">
      <img alt="nleanba logo" src="../assets/logo.png">
    </div>
    <div class="right">
      nleanba
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
}

.left {
  flex: 0 0.5 16rem;
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
  line-height: 8rem;
  padding: 4rem;
  font-size: 6rem;
  font-weight: 800;
}
</style>
