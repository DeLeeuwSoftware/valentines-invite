<script lang="ts">
  let button: HTMLButtonElement;
  let x = 0;
  let y = 0;

  function runAway() {
    const rect = button.getBoundingClientRect();
    const rectX = rect.x;
    const rectY = rect.y;
    const rectWidth = rect.width;
    const rectHeight = rect.height;

    let randomX = (Math.random() - 0.5) * 400;
    let randomY = (Math.random() - 0.5) * 400;
    
    if(rectX + randomX <= 0 || rectX + rectWidth + randomX >= window.innerWidth) {
      randomX *= -1;
    }
    if(rectY - (2 * rectHeight) + randomY <= 0 || rectY + randomY >= window.innerHeight) {
      randomY *= -1;
    }

    x = randomX;
    y = randomY;
  }
</script>

<div class="relative inline-block">
  <button
    bind:this={button}
    on:mouseenter={runAway}
    on:click={runAway} 
    style="transform: translate({x}px, {y}px);"
    class="
      px-8 py-3 
      bg-white text-rose-500 border-2 border-rose-200 
      hover:bg-rose-50 rounded-full font-bold transition-transform duration-200 ease-out
      shadow-sm select-none
    "
  >
    No
  </button>
</div>