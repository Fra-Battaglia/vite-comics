<script>
	export default {
		data() {
			return {
			}
		},
		props: {
			thumb: String,
			series: String,
		}
	}
</script>

<template>
	<div class="comic-card">
		<div class="comic-cover"><img :src="thumb" alt="copertina"></div>
		<div class="comic-title">{{ series }}</div>
	</div>
</template>

<style lang="scss" scoped>

	@use './styles/partials/mixins' as *;
	@use './styles/partials/variables' as *;

	.comic-card {
		width: 192px;
		margin-bottom: 2em;
	}

	img {
		width: 100%;
		height: 192px;
		object-fit: cover;
		object-position: top;
	}

	.comic-title {
		text-transform: uppercase;
	}
</style>