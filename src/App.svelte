<script>
  import Credential from './lib/components/Credential.svelte';
  import Skills from './lib/components/Skills.svelte';
  import Title from './lib/components/Title.svelte'
  import Presentation from './lib/components/Presentation.svelte';
  import { progress } from './lib/stores/progress';
  
  let progressCount;
  progress.subscribe(progress => {
    progressCount = progress
  })
</script>

<main style="padding:none;margin:none">
  {#if progressCount == 0}
    <div class="block">
      <Title/>
    </div>
  {:else if progressCount == 1}
    <div class="block">
      <Presentation/>  
    </div>
  {:else if progressCount == 2}
    <div class="block">
      <Skills/>
    </div>
  {:else}
    <div class="block">
      <Credential/>
    </div>
  {/if}
</main>

<style>
  .block{
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
