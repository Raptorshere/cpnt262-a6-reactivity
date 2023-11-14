<script>
	import Button from '../routes/button.svelte'
</script>

<Button>
	Toggle
</Button>

<style>
	:global(main) {
		background-color: #f2eee2;
		color: #0084f6;
		transition: background-color 0.3s
	}
	:global(main.dark-mode) {
		background-color: #1d3040;
		color: #bfc2c7;
	}
</style>