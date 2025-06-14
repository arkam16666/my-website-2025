<script>
	import '../app.css';
	import Nav from '$lib/components/Navbar.svelte';
	let { children } = $props();
</script>
<Nav/>
{@render children()}
