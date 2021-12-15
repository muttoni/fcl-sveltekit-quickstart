<script>
import { transactionStatus, transactionInProgress } from "../flow/stores";
</script>

<style>
  progress {
    margin-top:1em;
  }

  small {
    opacity:0.8;
  }
</style>
{#if $transactionInProgress}
<article class="card">
  Transaction status:
  {#if $transactionStatus < 2}
  <span><kbd>Pending</kbd><br/><small>The transaction has been received by a collector but not yet finalized in a block.</small></span>
  <progress indeterminate>Executing</progress>
  {:else if $transactionStatus === 2}
  <span><kbd>Finalized</kbd><br/><small>The consensus nodes have finalized the block that the transaction is included in.</small></span>
  <progress min="0" max="100" value="80">Executing...</progress>
  {:else if $transactionStatus === 3}
  <span><kbd>Executed</kbd><br/><small>	The execution nodes have produced a result for the transaction.</small></span>
  <progress min="0" max="100" value="80">Sealing...</progress>
  {:else if $transactionStatus === 4}
  <span><kbd>✓ Sealed</kbd><br/><small>The verification nodes have verified the transaction, and the seal is included in the latest block.</small></span>
  <progress min="0" max="100" value="100">Sealed!</progress>
  {:else}
  Expired!
  {/if}
</article>
{/if}