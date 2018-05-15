<template>
	<div>
		<v-btn color="success" @click="changeStep(step1, step2)">Success</v-btn>
	</div>
</template>

<script>
	export default {
		data () {
			return {
				step1: true,
				step2: false,
				step3: false
			}
		},
		methods: {
			changeStep: function(s1, s2) {
				debugger;
				this.s1 = false;
				this.s2 = true;
			}
		}
	}
</script>

<style scoped>

</style>


