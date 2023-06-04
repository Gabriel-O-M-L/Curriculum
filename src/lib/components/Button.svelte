<script>
	import {progress} from "../stores/progress" 
    import { slide } from "svelte/transition";
    let progressCount
    function next(){
        progress.update(n => n+1)
    }
    function back(){
        progress.update(n => n-1)
    }
    progress.subscribe(progress => (
        progressCount = progress
    ))
    function fadeSlide(node, options) {
		const slideTrans = slide(node, options)
		return {
			duration: options.duration,
			css: t => `
				${slideTrans.css(t,1)}
				opacity: ${t};
			`
		};
	}

</script>
<main>
    {#if progressCount != 0}
        <button in:fadeSlide={{duration:1000,axis:"x"}} out:fadeSlide={{duration:1000,axis:"-x"}} class="forward" style="transform: rotate(180deg);" on:click={back}/>
    {/if}
    {#if progressCount != 2}
        <button class="forward" style="right:0px" on:click={next}/>
    {/if}
</main>
<style>
    .forward{
        background-image: url("../../assets/arrow_forward.svg");
        height: 6%;
        top:45%;
        position: fixed;
        width: 50px;
        box-shadow: none;
        border: none;
        background-color: transparent;
    }
</style>