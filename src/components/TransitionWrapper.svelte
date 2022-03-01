<script>
  import { onMount } from "svelte";
  import { fly } from "svelte/transition";

  let show = false;

  onMount(() => {
    show = true;
  });
</script>

{#if show}
  <div class="transition" in:fly={{duration: 600,opacity: 0.05, }}>
    <slot />
  </div>
{/if}

<style>
  .transition {
    position: relative;
  }
</style>
