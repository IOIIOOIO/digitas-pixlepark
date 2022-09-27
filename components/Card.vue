<template>
	<article class="c-card">
		<img class="c-card__image" :src="image" :alt="alt" role="presentation"/>
		<h2 class="c-card__title">Test bane {{ name }}</h2>
		<p class="c-card__chip rounded-pill" :class="chipColorClass">Test color {{ color }} </p>
	</article>
</template>

<script>
	export default {
		name: "CCard",
		props: {
			image: {
				type: String,
				required: true
			},
			name: {
				type: String,
				required: true
			},
			level: {
				type: String,
				required: true
			},
		},
		computed: {
			chipColorClass() {
				return `u-bg-level-${this.level.toLowerCase()}`;
			}
		}
	}
</script>

<style scoped lang="scss">
	@import "~/assets/sass/1.settings/functions/get-map-val";
	@import "~/assets/sass/1.settings/functions/calc-rem";

	@import "~/assets/sass/1.settings/bootstrap-variables";
	@import "~bootstrap/scss/functions";
	@import "~bootstrap/scss/variables";
	@import "~bootstrap/scss/mixins";
	@import "~/assets/sass/1.settings/variables/colors";
	@import "~/assets/sass/1.settings/variables/spacers";
	@import "~/assets/sass/1.settings/variables/shadows";

	.c-card {
		display: flex;
		flex-direction: column;
		padding: $spacer-5 $spacer-5 $spacer-7;
		border-radius: $border-radius;
		background: linear-gradient(207.53deg, #FA00FF 0%, #5690FF 25.52%, #FA00FF 48.96%, #22B0FF 74.48%, #E600EB 100%);
		text-align: center;
		filter: drop-shadow($drop-shadow-md);
		&__image {
			margin-bottom: $spacer-5;
			border-radius: $border-radius;
		}
		&__title {
			margin-bottom: $spacer-6;
			font-weight: $font-weight-bolder;
		}
		&__chip {
			padding-right: $spacer-4;
			padding-left: $spacer-4;
			font-weight: $font-weight-bold;
			color: get-color(text, darkest);
		}
	}
</style>