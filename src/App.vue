<script>
	import AppHeader from './components/AppHeader.vue';
	import AppContent from './components/AppContent.vue';
	import AppPaneMenu from './components/AppPaneMenu.vue';
	import AppFooter from './components/AppFooter.vue';
	export default {
		components: {
			AppHeader,
			AppContent,
			AppPaneMenu,
			AppFooter
		}
	}
</script>

<template>
		<AppHeader />
		<main>
			<AppContent />
			<AppPaneMenu />
		</main>
		<AppFooter />
</template>

<style lang="scss">

	@use './components/styles/partials/mixins' as *;
	@use './components/styles/partials/variables' as *;

	@use './components/styles/generals.scss' as *;
</style>
