<template>
	<div>
		<c-search-input/>
		<div class="o-card-grid">
			<c-card name="Gabumon"
					image="https://digimon.shadowsmith.com/img/agumon.jpg"
					level="Rookie"/>
			<c-card name="Gabumon"
					image="https://digimon.shadowsmith.com/img/agumon.jpg"
					level="Rookie"/>
			<c-card name="Gabumon"
					image="https://digimon.shadowsmith.com/img/agumon.jpg"
					level="Rookie"/>
			<c-card name="Gabumon"
					image="https://digimon.shadowsmith.com/img/agumon.jpg"
					level="Rookie"/>
			<c-card name="Gabumon"
					image="https://digimon.shadowsmith.com/img/agumon.jpg"
					level="Rookie"/>
			<c-card name="Gabumon"
					image="https://digimon.shadowsmith.com/img/agumon.jpg"
					level="Rookie"/>
			<c-card name="Gabumon"
					image="https://digimon.shadowsmith.com/img/agumon.jpg"
					level="Rookie"/>
			<c-card name="Gabumon"
					image="https://digimon.shadowsmith.com/img/agumon.jpg"
					level="Rookie"/>
		</div>

	</div>

</template>

<script>
	import CCard from "../components/Card";
	import CSearchInput from "../components/SearchInput";

	export default {
		name: 'IndexPage',
		components: {CSearchInput, CCard},
	}
</script>

<style lang="scss" scoped>
	@import "~/assets/sass/1.settings/functions/get-map-val";
	@import "~/assets/sass/1.settings/functions/calc-rem";

	@import "~/assets/sass/1.settings/bootstrap-variables";
	@import "~bootstrap/scss/functions";
	@import "~bootstrap/scss/variables";
	@import "~bootstrap/scss/mixins";
	@import "~/assets/sass/1.settings/variables/breakpoint";
	@import "~/assets/sass/1.settings/variables/spacers";


	.o-card-grid {
		display: grid;
		grid-template-columns: 1fr;
		grid-row-gap: $spacer-17;
		grid-column-gap: $grid-gutter-width;
		@media #{$screen-md-up} {
			grid-template-columns: repeat(2, 1fr);
		}
		@media #{$screen-lg-up} {
			grid-template-columns: repeat(4, 1fr);
		}
	}
</style>
