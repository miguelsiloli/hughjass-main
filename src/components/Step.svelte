<script>
    export let step;
</script>

<a
    href={step.href}
    target="_blank"
    class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-blue-700 text-center cursor-pointer group hover:border-blue-400 duration-200"
    style="background-image: url({step.url}); background-size: cover; background-color: gray; background-blend-mode: multiply;"
    >
    <div
        class="bg-slate-950 grid place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200"
    >
        <i class={step.icon} />
    </div>
    <h3 class="font-medium text-xl sm:text-2xl md:text-3xl">
        {step.name}
    </h3>
    <slot />
    <div class="flex-1 flex items-end">
        <a
            href={step.href_github}
            target="_blank"
            class="flex items-center gap-2 cursor-pointer hover:text-blue-700 duration-300"
        >
            <span class="fa-brands fa-github" style="font-size: 1.5em;"></span>
        </a>
        {#if step.href_dashboard}
        <a
            href={step.href_dashboard}
            target="_blank"
            class="ml-auto flex items-center gap-2 cursor-pointer hover:text-blue-700 duration-300"
        >
            <span class="fa-solid fa-chart-line" style="font-size: 1.5em;"></span>
        </a>
        {/if}
        {#if step.href_notebooks}
        <a
            href={step.href_notebooks}
            target="_blank"
            class="ml-auto flex items-center gap-2 cursor-pointer hover:text-blue-700 duration-300"
        >
            <span class="fa-solid fa-book" style="font-size: 1.5em;"></span>
        </a>
        {/if}
    </div>
</a>
