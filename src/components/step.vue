<template>
	<div>
		<v-btn color="success" @click="step +'1'><slot></slot></v-btn>
	</div>
</template>

<script>
	export default {
		props: [step],
		data () {
			return {
			
			}
		}
	}
</script>

<style scoped>

</style>


