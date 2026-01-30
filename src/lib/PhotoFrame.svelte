<script lang="ts">
    export let src: string;
    export let alt: string = "Our Memory Together";
    export let caption: string = "";
    export let rotation: 'left' | 'right' | 'none' = 'none';
    const rotateClass = {
        left: '-rotate-2 hover:rotate-0',
        right: 'rotate-2 hover:rotate-0',
        none: 'hover:scale-105'
    }[rotation];
</script>