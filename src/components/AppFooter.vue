<script>
	export default {
		data() {
			return {
				Links: [
					{
						menu_title: 'DC COMIX',
						menu_links: [
							'Characters',
							'Comics',
							'Movies',
							'TV',
							'Games',
							'Videos',
							'News'
						]
					},
					{
						menu_title: 'SHOP',
						menu_links: [
							'Shop DC',
							'Shop DC Collectibles',
						]
					},
					{
						menu_title: 'DC',
						menu_links: [
							'Terms Of Use',
							'Privacy policy (New)',
							'Ad Choices',
							'Advertising',
							'Jobs',
							'Subscriptions',
							'Talent Workshops',
							'CPSC Certificates',
							'Ratings',
							'Shop Help',
							'Contact Us',
						]
					},
					{
						menu_title: 'SITES',
						menu_links: [
							'DC',
							'MAD Magazine',
							'DC Kids',
							'DC Universe',
							'DC Power Visa',
						]
					},
				],

				Socials: [
					{
						social: 'facebook',
						icon: './src/assets/img/footer-facebook.png'
					},
					{
						social: 'twitter',
						icon: './src/assets/img/footer-twitter.png'
					},
					{
						social: 'youtube',
						icon: './src/assets/img/footer-youtube.png'
					},
					{
						social: 'pinterest',
						icon: './src/assets/img/footer-pinterest.png'
					},
					{
						social: 'periscope',
						icon: './src/assets/img/footer-periscope.png'
					},
				]
			}
		}
	}
</script>

<template>
	<footer>
		<div class="footer-links">
			<div class="container">
				<div v-for="(item, index) in Links" :key="index" class="link-list">
					<h3>{{ item.menu_title }}</h3>
					<ul>
						<li v-for="(item2, index2) in item.menu_links" :key="index2">
							<a href="#">{{ item2 }}</a>
						</li>
					</ul>
				</div>
			</div>
		</div>
		<div class="follow-us">
			<div class="container">
				<a href="#" class="sign-up">SIGN-UP NOW!</a>

				<div class="social">
					<h3>FOLLOW US</h3>
					<a href="#" v-for="(item, index) in Socials" :key="index"><img :src="item.icon" :alt="item.social" /></a>
				</div>
			</div>
		</div>
	</footer>
</template>

<style lang="scss" scoped>
	@use './styles/partials/mixins' as *;
	@use './styles/partials/variables' as *;

	.footer-links {
		background-image: url(../assets/img/footer-bg.jpg);
		background-size: cover;
		.container {
			background-image: url(../assets/img/dc-logo-bg.png);
			background-repeat: no-repeat;
			background-position: right center;
			height: 100%;
			padding: 2em 0;
			display: flex;
			gap: 2em;

			.link-list {
				h3 {
					color: $light-color;
					margin-bottom: 0.5em;
				}

				a {
					color: $grey-color;
					line-height: 1.5;
				}

				a:hover {
					text-decoration: underline;
				}
			}
		}
	}
	.follow-us {
		padding: 1em;
		background-color: #2E2E2E;

		.container {
			@include flex-space-between;
			.sign-up {
				border: 2px solid $primary-color;
				color: $light-color;
				padding: 1em;
				display: inline-block;
				font-weight: 700;
				transition: 0.3s;
			}

			.sign-up:hover {
				background-color: $primary-color;
			}

			.social {
				@include flex-align-items-center;
				@include flex-space-between;
				gap: 1em;

				h3 {
					color: $primary-color;
				}
			}
		}
		
	}
</style>