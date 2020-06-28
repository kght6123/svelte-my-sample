<script>
	export let name;
	import Nested from './Nested.svelte';
	import WriteHtmlTag from './WriteHtmlTag.svelte';
	import InnerHtmlTag from './InnerHtmlTag.svelte';
	import ReactivityCountUp from './ReactivityCountUp.svelte';
	import ReactivityUpdateArrayAndObject from './ReactivityUpdateArrayAndObject.svelte';
	import SpreadProps from './SpreadProps.svelte'
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<InnerHtmlTag />
	<WriteHtmlTag html={"this string contains some <strong>HTML!!!</strong>"}/>
	<WriteHtmlTag />
	<ReactivityCountUp />
	<ReactivityUpdateArrayAndObject />
	<SpreadProps />
	<Nested />
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