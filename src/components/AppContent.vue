<script>
	export default {
		data() {
			return {
				Message: '-->> Content Goes Here <<--'
			}
		}
	}
</script>

<template>
	<div class="content">
		<div class="container">
			<h1>{{ Message }}</h1>
		</div>
	</div>

</template>

<style lang="scss" scoped>

	@use './styles/partials/mixins' as *;
	@use './styles/partials/variables' as *;

	.content {
		height: 100px;
		background-color: $dark-color;
		color: $light-color;
		@include flex-align-items-center;
	}
</style>