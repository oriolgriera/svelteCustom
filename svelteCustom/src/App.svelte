<script>
	import { Button, Input} from 'proi-ui'
	export let name  = "";
	export let familyname  = "";
	export let submit = false;
	
	function submitInfo() {
		submit = true;
	}

	function resetInfo() {
		submit = false;
		name  = "";
		familyname  = "";
	}
	</script>

<main>
	<Input label="Name" bind:value={name}/>
	<Input label="Family Name" bind:value={familyname}/>
	<Button on:click={submitInfo}>Submit</Button>
	<Button type="secondary" on:click={resetInfo}>Reset</Button>
	{#if submit}
	<p>Your name is {name} and your family name is {familyname}.</p>
	<!-- <Alert type="success">Correctly Submitted</Alert> -->
    {:else}
	<p>Please submit the info.</p>
    {/if}
</main>