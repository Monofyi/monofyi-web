<script setup>
import TheWelcome from '@/components/TheRegister.vue'
</script>

<template>
	<header>
		<RouterLink class="title" to="/">Monofyi</RouterLink>
	</header>
  <main>
    <TheWelcome />
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

</style>
