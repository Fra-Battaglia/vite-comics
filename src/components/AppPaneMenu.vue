<script>
	export default {
		data() {
			return {
				menu_options: [
					{
						option: 'DIGITAL COMICS',
						icon: './src/assets/img/buy-comics-digital-comics.png'
					},
					{
						option: 'DC MERCHANDISE',
						icon: './src/assets/img/buy-comics-merchandise.png'
					},
					{
						option: 'SUBSCRIPTION',
						icon: './src/assets/img/buy-comics-subscriptions.png'
					},
					{
						option: 'COMIC SHOP LOCATOR',
						icon: './src/assets/img/buy-comics-shop-locator.png'
					},
					{
						option: 'DC POWER VISA',
						icon: './src/assets/img/buy-dc-power-visa.svg'
					},
				]
			}
		}
	}
</script>

<template>
	<div class="pane-menu">
		<div class="container">
			<ul>
				<li v-for="(item, index) in menu_options" :key="index">
					<a href="#">
						<img :src="item.icon" :alt="option">
						{{ item.option }}
					</a>
				</li>
			</ul>
		</div>
	</div>
</template>

<style lang="scss" scoped>

	@use './styles/partials/mixins' as *;
	@use './styles/partials/variables' as *;
	.pane-menu {
		background-color: $primary-color;
		padding: 4em 0;

		ul {
			@include flex-space-between;
			
			li {
				a {
					@include flex-align-items-center;
					color: $light-color;

					img {
						height: 60px;
						display: block;
						margin-right: 1em;
					}
				}
			}

			li:last-child {
				img {
					width: 80px;
				}
			}
		}
	}
</style>