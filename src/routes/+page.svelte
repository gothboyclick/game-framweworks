<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import Jogo from './jogo.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
		<div class="logo"></div>
<a href="/jogo">
	<div class="box-game">
 <Jogo />
</div>
</a>

	
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.box-game {
		width: 900px;
		height: 510px;
		background: transparent;
		background-image: url('src/bg.png');
		background-size: contain;
		background-repeat: no-repeat;
		transition: all 1.7s;
		filter:blur(7px)
	}

	.box-game:hover {
		width: 900px;
		height: 510px;
		background: transparent;
		background-image: url('src/bg-over.png');
		background-size: contain;
		background-repeat: no-repeat;
		filter: grayscale(0);
		filter:blur(0px)
	}

	.logo {
		width:360px;
		height: 100px;
		background: transparent;
		background-image: url('src/logo.png');
		background-size: contain;
		background-repeat: no-repeat;
	}
</style>
