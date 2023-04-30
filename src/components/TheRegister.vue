<script setup>
const dark_mode = window.matchMedia("(prefers-color-scheme: dark)").matches;
</script>

<template>
	<div class="register">
		<div class="register-container">
			<h1 class="register-container-title">
				Connect with your FMCG distributors through a single platform.
			</h1>
			<p class="register-container-description">
				With Monofyi, you can easily manage your product catalog, track margins,
				place orders, and stay on top of pending payments, all in a single,
				user-friendly interface.
			</p>
			<div class="register-cta">
				<button class="register-cta-btn">Register for launch updates.</button>
				<p class="register-cta-details">
					for any question:
					<a
						href="mailto:harshit@monofyi.com"
						class="register-cta-link">
						harshit@monofyi.com
					</a>
				</p>
			</div>
		</div>
		<div class="register-schema">
			<p>Distributors</p>
			<img
				class="register-schema-svg"
				:src="'assets/schema_' + (dark_mode ? 'dark' : 'light') + '.webp'"
				alt="schema"
			/>
			<p>Buyers</p>
		</div>
	</div>
</template>

<style lang="scss">

.register {
	padding: 0 160px;
	display: flex;
	justify-content: space-between;
	gap: 120px;

	&-container {
		display: flex;
		flex-direction: column;
		justify-content: center;
		gap: 55px;

		&-title {
			margin: 0;
			font-family: 'Alata', sans-serif;
			font-size: 48px;
		}

		&-description {
			margin: 0;
			color: var(--text-secondary);
			line-height: 100%;
		}
	}

	&-cta {
		width: fit-content;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;

		&-btn {
			font-family: 'Alata', sans-serif;
			font-size: 32px;

			padding: 42px 95px;
			background: var(--btn-bg);
			color: var(--btn-text);

			border: 0;
			border-radius: 5em;
		}

		&-details {
			font-family: 'Alata', sans-serif;
			font-size: 20px;
		}

		&-link {
			color: var(--accent);
		}
	}

	&-schema {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;

		&-svg {
			height: 495px;
			aspect-ratio: 1/1;
		}
	}
}

</style>
