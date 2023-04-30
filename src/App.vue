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
}

:root {
	--bg-dark-mode: var(--palette-dark-blue);
	--bg-light-mode: var(--palette-white);

	--text-title-dark-mode: var(--palette-white);
	--text-title-light-mode: var(--palette-grey);

	--btn-bg-light-mode: var(--palette-dark-blue);
	--btn-text-light-mode: var(--palette-white);

	--btn-bg-dark-mode: var(--palette-white);
	--btn-text-dark-mode: var(--palette-dark-blue);

	--text-secondary: var(--palette-grey);
	--accent: var(--palette-orange);

	--bg: var(--bg-light-mode);
	--text-title: var(--text-title-light-mode);

	--btn-bg: var(--btn-bg-light-mode);
	--btn-text: var(--btn-text-light-mode);
}

@media (prefers-color-scheme: dark) {
	:root {
		--bg: var(--bg-dark-mode);
		--text-title: var(--text-title-dark-mode);

		--btn-bg: var(--btn-bg-dark-mode);
		--btn-text: var(--btn-text-dark-mode);
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
