<template name="button1">
	<v-card-actions>
		<v-btn color="success" @click="nextStep"> >>> </v-btn>
		<v-btn color="danger" @click="prevStep"> //// </v-btn>
	</v-card-actions>
</template>

<script>
	export default {
		data() {
			return {
				currentStep: "step1"
			}
		},
		methods: {
			nextStep: function () {
				debugger;
				this.$emit('changeStep', this.currentStep++)
			},
			prevStep: function () {
				this.$emit('changeStep', this.currentStep--)
			}
		}
	}
</script>

<style scoped>

</style>


