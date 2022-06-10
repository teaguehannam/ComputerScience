<script>
	import { url } from "@roxi/routify";
	import { sites } from '../sites.js';
</script>


<header>
	{#each sites as s}
		<a href={s.url} >{s.id}</a>
	{/each}
</header>

<slot />

<footer>
	<img src='./gear.png' alt='Settings' />
</footer>


<style lang=scss>
	header {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		text-align: center;

		a {
			display: block;
			background: rgba(240,240,240,0.7);
			color: rgba(30,130,31,1);
			font-size: calc(1rem + 2vw);
			text-decoration: none;
			padding: 9px 0;
		}

	} // main


	footer {
		position: fixed;
		bottom: 0;
		left: 0;

		img {
			box-shadow: 0 0 -3px 12px rgba(30,31,33,0.5);
			height: 64px;
			padding: 0 8px;
		}
	}
</style>

