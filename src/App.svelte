<script>
  import Credential from './lib/components/Credential.svelte';
  import Skills from './lib/components/Skills.svelte';
  import Title from './lib/components/Title.svelte'
  import { progress } from './lib/stores/progress';
  
  let progressCount;
  progress.subscribe(progress => {
    progressCount = progress
  })
</script>

<main style="padding:none;margin:none">
  {#if progressCount == 0}
  <div class="title">
    <Title/>
  </div>
  {:else if progressCount == 1}
    <Skills/>
  {:else}
    <Credential/>
  {/if}
</main>

<style>
  .title{
    background-color: red;
    height: 100%;
    width: 100%;
    position: fixed;
    top:0px;
    left:0px;
  }
  *{
    margin: none;
  }

</style>
