<template>
<main>
  <section class="white">
    <h2>Open-Source–Projects I’m Contributing to:</h2>
  </section>
  <section v-for="project in projects" :key="project.name">
    <h3>{{ project.name }}</h3>
    <blockquote v-html="project.quote" />
    <p v-for="(t, i) in project.description" :key="i" v-html="t"/>
  </section>
  <section class="white">
    <div>and more...</div>
  </section>
  <section>
    <h2>Links</h2>
    <ul>
      <li><a href="https://github.com/nleanba">Github Profile</a></li>
      <li><a href="https://factsmission.com/">FactsMission Website</a></li>
    </ul>
  </section>
</main>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Main extends Vue {
  projects: {
      name: string;
      description: string[];
      quote?: string;
    }[] = [
    {
      name: 'tridoc',
      quote: 'Tridoc aims to provide easy document management for individuals and small teams.',
      description: [
        'Documents can be accessed in the browser via a <a href="https://github.com/tridoc/tridoc-cockpit">web interface</a>.',
        'On the server-side, Tridoc runs using hapijs in node and fuseki. <a href="https://github.com/tridoc/tridoc-backend">View the repository of the backend.</a>',
        'There also exists <a href="https://github.com/tridoc/tridoc-folder">a native program</a> for easy upload from a folder on your computer. It doesn’t, however, provide any graphical user interface (yet?).',
        'Tridoc is mostly written and maintained by me.']
    },
    {
      name: 'SynoSpecies',
      quote: 'Synospecies is a tool developed by FactsMission AG to leverage the RDF data provided by <a href="https://plazi.org/">Plazi</a>. The RDF data of all treatments is stored in an <a href="https://allegrograph.com/">AllegroGraph</a> triple store allowing <a href="https://www.w3.org/TR/sparql11-overview/">SPARQL</a> queries over the data. Synospecies allows manually writing and submitting such queries in the advanced mode and send such queries in the background when using the easier interface.</blockquote>',
      description: [],
    }
  ]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@use '../vars';

section {
  padding: 1rem;
  & > * {
    max-width: 50rem;
    margin: 1rem auto;
  }
}

section:nth-child(2n+1) {
  background-color: vars.$c_10;
}

section:nth-child(2n+0) {
  background-color: vars.$c_20;
  //color: #ffffff;
}

section.white {
  background-color: #ffffff;
  color: #000000;
}

blockquote {
  padding: 0 0 0 1rem;
  border-left: 3px solid vars.$c_40;
}
</style>
