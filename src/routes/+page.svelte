<script lang="ts">
import ValentineWrapper from '$lib/components/ValentineWrapper.svelte';
import PhotoFrame from '$lib/components/PhotoFrame.svelte';
import RunawayButton from '$lib/components/RunawayButton.svelte';
import weddingDress from '$lib/assets/20230430_095949.jpg';
import haiku from '$lib/assets/20230614_164328.jpg';
import puppyLove from "$lib/assets/20240715_111343.jpg";
import vampire from "$lib/assets/20250106_200757.jpg";
import beautifulBlackJumper from "$lib/assets/20250726_124407.jpg";
import sillyCow from "$lib/assets/20250726_142453.jpg";
import sneaslebutt from "$lib/assets/20250924_210536.jpg";
import sillyFace from "$lib/assets/20251004_143350.jpg";
import flying from "$lib/assets/20251007_121917.jpg";
import patpat from "$lib/assets/20251007_153725.jpg";
import chestnutHoarder from "$lib/assets/20251027_211317.jpg";
import happyFamily from "$lib/assets/20251212_162403.jpg";
import funnySmile from "$lib/assets/20251223_200617.jpg";
import soccyPuppy from "$lib/assets/20260124_095432.jpg";

let isValentine = false;
function celebrate() {
    isValentine = true;
}
</script>

<ValentineWrapper>
    <h1 class="text-rose-500 font-bold pb-4 text-3xl">Will you be my Valentine?</h1>
    {#if !isValentine}
        <div class="relative inline-block">
            <button
                on:click={celebrate} 
                class="
                px-8 py-3 
                bg-white text-rose-500 border-2 border-rose-200 
                hover:bg-rose-50 rounded-full font-bold transition-transform duration-200 ease-out
                shadow-sm select-none
                "
            >
                Yes ❤️
            </button>
        </div>
        <RunawayButton />
    {:else}
        <p class="text-rose-500 font-bold pb-4">Yay! I Love You!!! ❤️</p>
        <div class="photo-gallery">
            <PhotoFrame src={weddingDress} alt="Wedding Dress" caption="Getting Ready for the photos!" tilt="left" />
            <PhotoFrame src={haiku} alt="Haiku" caption="Anniversary!" tilt="right" />
            <PhotoFrame src={puppyLove} alt="Puppy Love" caption="Puppy Love" />
            <PhotoFrame src={vampire} alt="Vampire" caption="Vampire" />
            <PhotoFrame src={beautifulBlackJumper} alt="Beautiful Black Jumper" caption="Beautiful Black Jumper" tilt="left" />
            <PhotoFrame src={sillyCow} alt="Silly Cow" caption="Silly Cow" tilt="right" />
            <PhotoFrame src={sneaslebutt} alt="Sneaslebutt" caption="Sneaslebutt" />
            <PhotoFrame src={sillyFace} alt="Silly Face" caption="Silly Face" />
            <PhotoFrame src={flying} alt="Flying" caption="Flying" tilt="left" />
            <PhotoFrame src={patpat} alt="Patpat" caption="Patpat" tilt="right" />
            <PhotoFrame src={chestnutHoarder} alt="Chestnut Hoarder" caption="Chestnut Hoarder" />
            <PhotoFrame src={happyFamily} alt="Happy Family" caption="Happy Family" />
            <PhotoFrame src={funnySmile} alt="Funny Smile" caption="Funny Smile" tilt="left" />
            <PhotoFrame src={soccyPuppy} alt="Soccy Puppy" caption="Soccy Puppy" tilt="right" />
        </div>
    {/if}


</ValentineWrapper>