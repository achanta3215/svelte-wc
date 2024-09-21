<svelte:options customElement="sv-avatar" />

<script lang="ts">
  export let name: string;
  export let url: string;
</script>

<style>
  .avatar {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #f0f0f0;
    font-size: 24px;
    color: #555;
  }
  
  .avatar img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
</style>

<div class="avatar">
  {#if url}
    <img src={url} alt={name} />
  {:else}
    {name ? name[0] : "?"}
  {/if}
</div>