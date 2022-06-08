<script lang="ts">
	import Fab, { Icon } from '@smui/fab';
	import Counter from '$lib/Counter.svelte';
	import {isOverlayOpen} from "../stores/overlay";
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Pixotronics" />
	<!-- Fonts -->
  	<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
	
  	<!-- Material Typography -->
	<link rel="stylesheet" href="https://unpkg.com/@material/typography@13.0.0/dist/mdc.typography.css" />
	
	<!-- SMUI -->
	<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/svelte-material-ui@6.0.0-beta.4/bare.min.css" />
</svelte:head>
<section class="bglayout">
	<div>
		<h2 class="bg1">Jewelery Shop</h2>
		<div class="py-4">Categories About Shop</div>		
	</div>
	<Fab variant="raised" color="primary" on:click={() => {isOverlayOpen.set(true)}}>
		<Icon class="material-icons">send</Icon>
	</Fab>
</section>

<style>
	section {
		display: flex; 
		justify-content: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}

	.bglayout{
		background-color: bisque;
		display: flex;
		flex-direction: row;
    	padding: 0px 100px;
		text-align: left;
	}

	.welcome {
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
	
	.bg1{
		align-items: left;
	}
	.button { 
		background-color: aqua;
		color: aliceblue;
		
	}
</style>
