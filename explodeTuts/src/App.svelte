<script>
	import Header from "./components/Header.svelte";
	import Footer from "./components/Footer.svelte";
	import RootFile from "./datepicker/RootFile.svelte";
	export let name;
</script>

<style>
	main {
		max-width: 960px;
		margin: 40px auto;
	}
	p {
		text-align: center;
	}
</style>

<Header />
<main>
	<p>
		Welcome to the Official Booking System for Explode Studios! Use this
		system to see availability and book your session.
	</p>
	<RootFile />
</main>
<Footer />
