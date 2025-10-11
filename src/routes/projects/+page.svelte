<script>
    import { projects } from '$lib/data/projects';
    import ProjectCard from '$lib/components/Project.svelte';
</script>

<div class="container mx-auto px-6 py-16">
    <header class="text-center mb-12">
        <h1 class="text-5xl font-extrabold text-gray-900 mb-4">My Portfolio</h1>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
            A collection of my personal projects
        </p>
    </header>

    <div class="grid gap-10 md:grid-cols-2 lg:grid-cols-3">
        {#each projects as project (project.title)}
            <ProjectCard {project} />
        {/each}
    </div>
</div>