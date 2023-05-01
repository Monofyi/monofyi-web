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
