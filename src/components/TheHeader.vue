<script setup>
defineProps(["toggler", "dark_mode"]);
</script>

<template>
	<header>
		<RouterLink class="title" to="/">Monofyi</RouterLink>
		<div id="theme-btn" :key="dark_mode" @click="toggler()">
			<img v-if="dark_mode" src="assets/sun.svg" alt="Toggle light theme">
			<img v-else src="assets/moon.svg" alt="Toggle dark theme">
		</div>
	</header>
</template>

<style lang="scss">

header {
	display: flex;
	justify-content: space-between;
	align-items: center;
}

.title {
	color: var(--accent);
	font-family: 'Righteous', cursive;
	text-decoration: none;
}

#theme-btn {
	display: flex;
	cursor: pointer;

	img {
		width: 1.2em;
		height: 1.2em;
	}
}
</style>
