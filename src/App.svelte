<script>
	import Home from './Pages/Home.svelte'
	import About from './Pages/About.svelte'
	import Skills from './Pages/Skills.svelte'
	import Hacks from './Pages/Hacks.svelte'
	import Contact from './Pages/Contact.svelte'
	import NavBar from './Components/NavBar.svelte'
</script>

<main>
	<NavBar/>
	<div class = "pages">
		<Home/>
		<About/>
		<Skills/>
		<Hacks/>
		<Contact/>
	</div>
</main>

<style>
	.pages{
		overflow-y: scroll;
  		height: 100vh;
  		scroll-snap-points-y: repeat(100vh);
  		scroll-snap-type: y mandatory;
  		color: white;
  		box-sizing: border-box;
  		text-align: center;
  		scroll-behavior: smooth;
	}
</style>