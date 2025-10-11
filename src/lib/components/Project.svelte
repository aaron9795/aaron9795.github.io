<script>
    export let project;
</script>

<div class="bg-white rounded-xl shadow-lg hover:shadow-2xl transition duration-300 overflow-hidden border border-gray-100">
    <div class="bg-gray-200 h-48 w-full flex items-center justify-center">
        <p class="text-gray-500 font-medium">Image/Viz Screenshot Here</p>
        </div>

    <div class="p-6">
        <h3 class="text-2xl font-bold mb-2 text-gray-800">{project.title}</h3>
        <p class="text-gray-600 mb-4">{project.description}</p>

        <div class="flex flex-wrap gap-2 mb-4">
            {#each project.technologies as tech}
                <span class="text-xs font-semibold px-3 py-1 bg-blue-100 text-blue-800 rounded-full">
                    {tech}
                </span>
            {/each}
        </div>
        <div class="flex space-x-3 mt-4">
            {#if project.liveUrl}
                <a 
                    href={project.liveUrl} 
                    target="_blank" 
                    rel="noopener noreferrer"
                    class="px-4 py-2 bg-blue-600 text-white text-sm font-medium rounded-lg hover:bg-blue-700 transition"
                >
                    Live Demo ↗
                </a>
            {/if}
            <a 
                href={project.githubUrl} 
                target="_blank" 
                rel="noopener noreferrer"
                class="px-4 py-2 border border-gray-300 text-gray-700 text-sm font-medium rounded-lg hover:bg-gray-100 transition"
            >
                GitHub Code 📦
            </a>
        </div>
    </div>
</div>