<script>
	import { fade,fly } from 'svelte/transition';
  import { onMount } from 'svelte';
  import Button from './Button.svelte';
	let visible = false;
  const activate = () => {
    visible = true
  }
  onMount(()=>{
    setTimeout(activate,400)
  })
</script>
<main>
{#if visible}
	<div class="title">
		<ul class="presentation">
      <li transition:fade>Gabriel Oliveira Moura Lima</li>
      <li in:fly="{{y:10 , duration:2000}}">Who am I?</li>
    </ul>
    <Button/>
  </div>
{/if}

</main>

<style>
  @import url('https://fonts.cdnfonts.com/css/league-gothic-3');
  .title{
    position: relative;
    margin: none;
    padding: none;
  }
  .presentation{
    list-style: none;
    background-color: white;
    position: fixed;
    text-align: center;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    width: 100%;
  }
  
  li{
    font-family: 'League Gothic', sans-serif;
    font-size: 50px;
  }
</style>