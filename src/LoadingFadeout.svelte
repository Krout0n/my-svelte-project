<script>
  import Loading from "./Loading.svelte";
  let visible = true;
  setTimeout(() => {
    visible = false;
  }, 3400);
</script>

{#if visible}
  <Loading period={"1.7s"} />
{:else}
  <!-- ロードが終わった後に表示するコンポーネント -->
  <slot />
{/if}
