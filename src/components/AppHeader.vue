<script>
	export default {
		data() {
			return {

				menu_voices: [
					{
						voice: 'CHACRACTERS',
						active: false
					},
					{
						voice: 'COMICS',
						active: true
					},
					{
						voice: 'MOVIES',
						active: false
					},
					{
						voice: 'TV',
						active: false
					},
					{
						voice: 'GAMES',
						active: false
					},
					{
						voice: 'COLLECTIBLES',
						active: false
					},
					{
						voice: 'VIDEOS',
						active: false
					},
					{
						voice: 'FANS',
						active: false
					},
					{
						voice: 'NEWS',
						active: false
					},
					{
						voice: 'SHOP',
						active: false
					},
				]
			}
		}
	}
</script>

<template>
	<header>
		<div class="container">
			<img src="../assets/img/dc-logo.png" alt="logo dc"/>
	
			<ul>
				<li v-for="(item, index) in menu_voices" :key="index" :class="item.active ? 'active' : ''"><a href="#" class="">{{ item.voice }}</a></li>
			</ul>
		</div>
	</header>

</template>

<style lang="scss" scoped>

	@use './styles/partials/mixins' as *;
	@use './styles/partials/variables' as *;

	.container {
		@include flex-space-between;
	}

	img {
		padding: 1em 0
	}

	ul {
		@include flex-space-between;
		list-style: none;
		font-weight: 700;
		width: 70%;

		li {
			height: 100%;
			@include flex-align-items-center;
			border-bottom: 5px solid transparent;
			border-top: 5px solid transparent;

			a {
				color: $dark-color;
				text-decoration: none;
			}
		}

		li.active {
			border-bottom-color: $primary-color;

			a {
				color: $primary-color;
			}
		}
	}

</style>