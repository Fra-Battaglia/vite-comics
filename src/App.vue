<script>
	import AppHeader from './components/AppHeader.vue';
	import AppContent from './components/AppContent.vue';
	import AppPaneMenu from './components/AppPaneMenu.vue';
	export default {
		components: {
			AppHeader,
			AppContent,
			AppPaneMenu
		}
	}
</script>

<template>
		<AppHeader />
		<main>
			<AppContent />
			<AppPaneMenu />
		</main>
</template>

<style lang="scss">

	@use './components/styles/partials/mixins' as *;
	@use './components/styles/partials/variables' as *;

	@import url('./components/styles/generals.scss');
</style>
