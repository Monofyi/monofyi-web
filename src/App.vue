<script setup>
import { RouterView } from 'vue-router'
</script>

<template>
  <RouterView />
</template>

<style lang="scss">

:root {
	--palette-white: white;
	--palette-dark-blue: #060F1C;
	--palette-orange: #FC7424;

	--palette-dark-grey: #434343;
	--palette-grey: #828282;

	--bg-dark-mode: var(--palette-dark-blue);
	--bg-light-mode: var(--palette-white);

	--text-title-dark-mode: var(--palette-white);
	--text-title-light-mode: var(--palette-grey);

	--text-secondary: var(--palette-grey);
	--accent: var(--palette-orange);


	@media (prefers-color-scheme: dark) {
		--text-title: var(--text-title-dark-mode);
		--bg: var(--bg-dark-mode);
	}

	@media (prefers-color-scheme: light) {
		--text-title: var(--text-title-light-mode);
		--bg: var(--bg-light-mode);
	}
}

body {
	color: var(--text-secondary);
	background: var(--bg);

	font-family: 'Alata', sans-serif;
	font-size: 28px;

	box-sizing: border-box;
	height: 100vh;
	padding: 2em;
	margin: 0;
}

#app {
	height: 100%;

	display: flex;
	flex-direction: column;

	align-content: space-between;
	justify-content: space-between;
}

</style>
