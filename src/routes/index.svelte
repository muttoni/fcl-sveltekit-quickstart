
<script>
	import Auth from '$lib/Auth.svelte';
  import Transaction from '$lib/Transaction.svelte';

</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<div class="mb-2">
  <Transaction />
</div>

<Auth/>
