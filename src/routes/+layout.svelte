<script lang="ts">
	import '../app.postcss';
	import Sidebar from './Sidebar.svelte';
	import NavBar from './NavBar.svelte';

	let isOpen = false;
</script>

<heder>
	<NavBar bind:isOpen />
	<Sidebar {isOpen} />
</heder>
<main>
	<slot />
</main>
<footer />
