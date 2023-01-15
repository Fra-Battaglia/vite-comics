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
			<h2 class="title-label">CURRENT SERIES</h2>
			<div class="comics-list">
				<AppCard v-for="(item, index) in ComicData" :key="index" :thumb="item.thumb" :series="item.series" />
				<div  class="load-more">
					<a href="#">LOAD MORE</a>
				</div>
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
		
		.container {
			position: relative;
			.title-label {
				position: absolute;
				transform: translateY(-50%);
				background-color: $primary-color;
				padding: 0.5em 1em;
				left: -1em;
			}
			.comics-list {
				@include flex-space-between;
				padding: 4em 0;
				flex-wrap: wrap;
			}
			.load-more {
				width: 100%;
				display: flex;
				
				a {
					margin: 0 auto;
					padding: 0.5em 2em;
					background-color: $primary-color;
					color: $light-color;
					font-weight: 700;
				}
			}
		}
	}

</style>