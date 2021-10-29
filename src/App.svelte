<script>
	// export let name= 'Hello World';
	import Home from './Home.svelte';
	import News from './News.svelte';
	import Faculty from './Faculty.svelte';
	import Programs from './Programs.svelte';
	import Admission from './Admission.svelte';
	import Contact from './components/Contact.svelte';
	$: comp = 'Home';
	$: user = '';
	
</script>

<main>
	<h1> </h1>
	<div class="ui two column grid">
		<div class="row" >
		  <div class="twelve wide column"> 
			<button class="ui blue button"  on:click={() => comp='Home'}>Home</button>
			<button class="ui button"on:click={() => comp='News'}>Newsletter</button>
			<button class="ui blue button"on:click={() => comp='Programs'}>Programs</button>
			<button class="ui button"on:click={() => comp='Faculty'}>Faculty</button>
			<button class="ui blue button"on:click={() => comp='Admission'}>Admission</button>
			<button class="ui button" on:click={() => comp='Contact'} >Contact Us</button>
			</div>
			<div class = "four wide column"> 
				<h3> Welcome {user} </h3>
			 </div>
		</div>
		{#if comp =='Home'}
			<Home/>
		{:else if comp =='News'}
			<News/>
		{:else if comp =='Programs'}
			<Programs/>
		{:else if comp =='Admission'}
			<Admission/>
		{:else if comp =='Faculty'}
			<Faculty/>
		{:else if comp =='Contact'}
			<Contact/>
		{/if}
		<div class="four wide column"style = "border:1px solid black">
			<h3> Online Learning Portal</h3>
			<form class="ui form">
				<div class="field">
				  <label for="user">Username</label>
				  <input type="text" name="first-name" placeholder="First Name" bind:value={user}>
				</div>
				<div class="field">
				  <label for="pass">Password</label>
				  <input type="text" name="password" placeholder="password">
				</div>
				<button class="ui button" type="submit">Register</button>
			  </form>
		</div>
	</div>


</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>