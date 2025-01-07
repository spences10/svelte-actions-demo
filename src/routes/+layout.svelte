<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<main class="container prose-xl mx-auto mb-20 max-w-3xl flex-grow px-4">
	{@render children()}
</main>
