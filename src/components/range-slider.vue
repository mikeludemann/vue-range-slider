<template lang="html">

	<div class="range-slider">
		<input type="range" :id="id" :name="name" :min="min" :step="step" :max="max" @input="changeHandling" @change="changeHandling">
	</div>

</template>

<script lang="js">

	export default {
		name: 'rangeSlider',
		props: {
			id: String,
      name: String,
      min: String,
      max: String,
      step: String
		},
		mounted () {

		},
		data () {
			return {

			}
		},
		methods: {
			changeHandling ({ type, target }) {
				const event = {
					type,
					isCheckbox: target.type === 'checkbox',
					target: {
						value: target.value,
						checked: target.checked
					}
				}
				console.log(`${event.type}: ${event.isCheckbox ? event.target.checked : event.target.value}`);
			}
		},
		computed: {

		}
}


</script>

<style scoped lang="scss">
	.range-slider {

	}
</style>
