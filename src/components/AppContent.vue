<script>
	import ComicData from '../assets/data/dc-comics.json';
	import AppCard from './AppCard.vue';
	export default {
		data() {
			return {
				ComicData,

			}
		},

		components: {
			AppCard
		}
	}
</script>

<template>
	<div class="jumbotron"></div>

	<div class="current-series">
		<div class="container">
			<div class="comics-list">
				<AppCard v-for="(item, index) in ComicData" :key="index" :comic="item" />
			</div>
		</div>
	</div>

</template>

<style lang="scss" scoped>

	@use './styles/partials/mixins' as *;
	@use './styles/partials/variables' as *;

	.jumbotron {
		height: 400px;
		background-image: url(../assets/img/jumbotron.jpg);
		background-size: cover;
	}

	.current-series {
		color: $light-color;
		background-color: $dark-color;

		.comics-list {
			@include flex-space-between;
			flex-wrap: wrap;
		}
	}
</style>