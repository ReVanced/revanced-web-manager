<script lang="ts">
	import Button from '$lib/components/Button.svelte';
</script>

<section class="hero">
	<div class="hero-text">
		<h1>Continuing the <br />legacy of <span>Vanced.</span></h1>
		<p>
			Customize your mobile experience through ReVanced <br /> by applying patches to your applications.
		</p>
		<div class="hero-buttons">
			<Button icon="patch" type="filled" href="patch">Patch your app</Button>
			<Button icon="docs" type="tonal" href="docs">Documentation</Button>
		</div>
	</div>
</section>

<style>
	h1 {
		color: var(--white);
		margin-bottom: 1.5rem;
	}

	p {
		margin-bottom: 2rem;
	}

	.hero {
		padding-bottom: 9rem;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
		vertical-align: middle;
	}

	.hero-text {
		align-items: center;
	}

	.hero-buttons {
		display: flex;
		user-select: none;
		gap: 1rem;
	}

	span {
		color: var(--accent-color);
	}

	@media (max-width: 767px) {
		.hero {
			padding-bottom: 0;
		}

		br {
			content: ' ';
		}
	}

	@media screen and (max-width: 450px) {
		.hero-buttons {
			flex-direction: column;
		}
	}
</style>
