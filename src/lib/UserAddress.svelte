<script>
  import { user } from "../flow/stores";
</script>

<style>
  .led-green {
    position:relative;
    display:inline-block;
    top: 0px;
    margin-right:0.5em;
    background-color: var(--primary);
    width: 14px;
    height: 14px;
    border-radius: 14px;
  }
</style>

<div class="mb-1">
  {#if $user?.addr }
  <span class="led-green"></span>
  {/if}
  <span class="mono">{$user?.addr ?? "No Address"}</span>
</div>