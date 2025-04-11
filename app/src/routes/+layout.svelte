<script lang="ts">
	import '../app.css';
	import '@fontsource-variable/inter';
	import '@fontsource-variable/lexend';
	import Header from '../components/Header/Header.svelte';

	let { children } = $props();
</script>

<div class="bg-gray-950 text-white font-main">
	<Header />
	{@render children()}
</div>
