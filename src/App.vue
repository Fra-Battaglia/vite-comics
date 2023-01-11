<script>
	import AppHeader from './components/AppHeader.vue';
	import AppContent from './components/AppContent.vue';
	export default {
		components: {
			AppHeader,
			AppContent,
		}
	}
</script>

<template>
		<AppHeader />
		<AppContent />
</template>

<style lang="scss">

	@use './components/styles/partials/mixins' as *;
	@use './components/styles/partials/variables' as *;

	@import url('./components/styles/generals.scss');
</style>
