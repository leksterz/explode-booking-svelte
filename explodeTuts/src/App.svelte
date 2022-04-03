<script>
	import Header from "./components/Header.svelte";
	import Footer from "./components/Footer.svelte";
	export let name;
</script>

<style>
	main {
		max-width: 960px;
		margin: 40px auto;
	}
</style>

<Header />
<main>
	<p>
		Lorem ipsum, dolor sit amet consectetur adipisicing elit. Consequatur
		libero explicabo harum reprehenderit nesciunt eum animi excepturi nisi
		mollitia dolorem quia eos unde ipsum eaque maiores laboriosam ea,
		voluptates fuga?
	</p>
</main>
<Footer />
