<script lang="ts">
    export let vertical: boolean = false;

	interface Link {
		name: string;
		href: string;
	}

	let linkList: Link[] = [
		{ name: 'Home', href: '/' },
		{ name: 'About', href: '/about' },
		{ name: 'Services', href: '/contact' },
		{ name: 'Contact', href: '/contact' },

	];
</script>

<ul class="flex-grow flex {vertical ? 'flex-col' : ''} group justify-between items-center h-full w-full">
	{#each linkList as link}
		<li class="hover:scale-105 transition-all">
			<a href={link.href} class="text-slate-600 transition-all text-lg font-bold duration-300 hover:text-slate-900">
				{link.name}
			</a>
		</li>
	{/each}
</ul>