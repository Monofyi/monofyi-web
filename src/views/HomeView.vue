<script setup>
import TheRegister from '@/components/TheRegister.vue'
import { reactive } from 'vue'

const state = reactive({
  dark_mode:
    window.matchMedia(
			"(prefers-color-scheme: dark)"
    ).matches
})

function toggle_theme() {
	state.dark_mode = !state.dark_mode;

	let theme = state.dark_mode ? 'dark': 'light';

	console.log(`Switched ${theme} theme!`);
	document.documentElement.className = `theme-${theme}`;
}

</script>

<template>
	<header>
		<RouterLink class="title" to="/">Monofyi</RouterLink>
		<div id="theme-btn" :key="state.dark_mode" @click="toggle_theme()">
			<img v-if="state.dark_mode" src="assets/sun.svg" alt="Toggle light theme">
			<img v-else src="assets/moon.svg" alt="Toggle dark theme">
		</div>
	</header>
  <main>
    <TheRegister :key="state.dark_mode" :dark_mode="state.dark_mode" />
  </main>
	<footer>
		<p class="agreement">
			By continuing, you agree to the
			<RouterLink to="TermAndConditions">
				Terms & Conditions
			</RouterLink>
			and
			<RouterLink to="PrivacyPolicies">
				Privacy & Policies
			</RouterLink>
			of Bitecope Pvt Ltd.
		</p>
	</footer>
</template>


<style lang="scss">

header {
	display: flex;
	justify-content: space-between;
}

.title {
	color: var(--accent);
	font-family: 'Righteous', cursive;
	text-decoration: none;
}

.agreement {
	font-size: .6em;
	margin: 0;

	& > a {
		color: var(--accent);
	}
}

#theme-btn {
	display: flex;
	cursor: pointer;

	img {
		width: 1em;
		height: 1em;
	}
}
</style>
