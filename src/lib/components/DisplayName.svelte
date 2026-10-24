<script lang="ts">
	let firstName = $state('Amr');
	let lastName = $state('Elaraby');
	let fullName = $derived.by(() => {
		return `${firstName} ${lastName}`;
	});
	let username = $state('amrelaraby');

	$effect(() => {
		if (username || fullName) {
			console.log('User has a username or a fullname');
		}
	});
</script>

<input type="text" bind:value={username} />
<input type="text" bind:value={firstName} />
<input type="text" bind:value={lastName} />
<h1>{username || fullName}</h1>

<style>
	h1 {
		color: red;
	}
</style>
