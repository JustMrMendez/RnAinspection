<script lang="ts">
  import NavBar from './NavBar.svelte';

	import Logo from '$lib/Logo.svelte';
	import Links from '$lib/shared/Links.svelte';
	export let isOpen = false;
</script>

<div
	class="absolute right-0 z-10 h-screen pt-24 max-h-screen w-2/5 bg-slate-200 shadow-lg transition-all duration-300 md:hidden {isOpen
		? 'translate-x-[40vw%] opacity-100'
		: 'translate-x-[40vw] opacity-0'}"
>
	<div class="h-1/2">
        <Links vertical/>
    </div>
</div>

