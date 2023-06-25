<script>
    import {productCount} from "$lib/stores"
  import youpass from "$lib/images/you-pass.gif";
  import Incrimentor from "../../lib/components/Incrimentor.svelte";
  let showImage = false;
  function letMePass() {
    showImage = !showImage;
  }
  
</script>

<div>This is the AKAAT page!</div>

<a href="/">
  <button class="bg-blue-950 hover:bg-blue-950/50 text-white font-bold">
    Home
  </button>
</a>
<button
  class="bg-red-950 py-1 px-2 rounded-md hover:bg-red-950/50"
  type="button"
  on:click={letMePass}
>
  can I pass?
</button>
{#if showImage}
  <img class="w-[150px] aspect-auto" src={youpass} alt="" />
{/if}

<Incrimentor bind:count={$productCount}/>
<div>
  {$productCount}
</div>
