<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();

	const navLinks = [
    { name: 'Home', path: '/' },
    { name: 'Projects', path: '/projects' },
    { name: 'Data', path: '/data' },
    { name: 'About', path: '/about' },
  ];
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<header class="sticky top-0 z-50 bg-white shadow-md">
    <nav class="container mx-auto px-6 py-4 flex items-center justify-between">
        <a href="/" class="text-2xl font-bold text-gray-800 hover:text-blue-600 transition">
            Aaron Stocks
        </a>

        <div class="flex space-x-6">
            {#each navLinks as link}
                <a 
                    href={link.path}
                    class="text-gray-600 hover:text-blue-600 font-medium transition duration-150 ease-in-out"
                    data-sveltekit-reload
                >
                    {link.name}
                </a>
            {/each}
        </div>
    </nav>
</header>

{@render children?.()}


