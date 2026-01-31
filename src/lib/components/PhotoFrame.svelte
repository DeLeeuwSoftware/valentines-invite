<script lang="ts">
    export let src: string;
    export let alt: string = "Our Memory";
    export let caption: string = "";

    export let tilt: 'left' | 'right' | 'none' = 'none';
    const tiltClasses: Record<string, string> = {
        left: '-rotate-2 hover:rotate-0 hover:scale-105',
        right: 'rotate-2 hover:rotate-0 hover:scale-105',
        none: 'hover:scale-105'
    }
</script>
<div class="group relative bg-white p-3 sm:p-4 shadow-lg hover:shadow-2xl hover:z-20 rounded-sm transition-all duration-300 ease-out max-w-xs mx-auto {tiltClasses[tilt] || tiltClasses.none}">
<div class="aspect-[4/5] w-full overflow-hidden bg-gray-100 rounded-sm mb-3">
    <img {src} {alt} class="h-full w-full object-cover transition-transform duration-700 group-hover:scale-110"/>
</div>

{#if caption}
    <div class="text-center text-rose-600 font-handwriting text-3xl font-bold leading-none -rotate-1">
        {caption}
    </div>
{/if}

<div class="absolute -top-3 left-1/2 -translate-x-1/2 w-8 h-4 bg-white/40 border-l border-r border-white/50 shadow-sm backdrop-blur-[1px] rotate-2"></div>
</div>
