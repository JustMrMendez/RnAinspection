<script lang="ts">
	import Logo from '$lib/Logo.svelte';
	import Links from '$lib/shared/Links.svelte';
	export let isOpen = false;
</script>

<nav class="fixed z-20 flex w-full items-center justify-between bg-slate-200 px-10">
	<div class="h-16 w-16">
		<Logo {isOpen} />
	</div>
    <div class="hidden md:block">
        <Links />
    </div>
	<button on:click={() => (isOpen = !isOpen)} class="flex flex-col gap-1 md:hidden">
		<div
			class="h-1 w-6 rounded bg-slate-600 transition-all duration-300 {isOpen
				? '-rotate-45 translate-y-3 bg-slate-900'
				: 'bg-slate-600'}"
		/>
		<div
			class="h-1 w-6 rounded bg-slate-600 transition-all duration-300 {isOpen ? 'opacity-0' : ''}"
		/>
		<div
			class="h-1 w-6 rounded bg-slate-600 transition-all duration-300 {isOpen
				? 'rotate-45 -translate-y-1 bg-slate-900'
				: 'bg-slate-600'}"
		/>
	</button>
</nav>

