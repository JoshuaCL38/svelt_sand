<script>
    export let count
    function counter() {
    count = count + 1;
  }
</script>

<button on:click={counter}> +1 </button>
