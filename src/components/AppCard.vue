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

</style>