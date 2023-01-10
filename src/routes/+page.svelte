<script>
    import Button from './button.svelte';
    import Counter from './counter.svelte';
</script>
<div class="boddy">
    <div class="positioning">
        <Counter />
        <Button>
            Toggle!
        </Button>
    
    </div>
</div>

<style>
    .boddy {
        display: flex;
        width: 50%;
        margin: auto;
        border: solid;
        height: 300px;
    }
    .positioning {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        display: flex;
        flex-direction: column;
        width: fit-content;
        border: #000000;
        border: solid;
        border-radius: 5px;
        align-items: center;
    }
    :global(body) {
        margin: 0; padding: 0; 
    	background-color: #ffffff;
		transition: background-color 1.8s;
	}
	:global(body.dark-mode) {
		background-color: #1d3040;
	}
    
</style>