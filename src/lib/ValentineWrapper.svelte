<script lang="ts">
</script>
    <div class="flex justify-center w-full min-h-screen bg-rose-50">
        <aside class="w-[20px] shrink-0 bg-contain bg-repeat-y bg-right-top border-column"></aside>
        <main class="max-w-3xl px-8">
            <slot />
        </main>
        <aside class="w-[20px] shrink-0 bg-contain bg-repeat-y bg-left-top border-column"></aside>
    </div>

<style>
.border-column {
    background-image: url('$lib/assets/valentinesLine.svg');
}
</style>