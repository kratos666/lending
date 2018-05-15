<template>
	<v-app>
		<v-content>
			<v-container fluid>
				<step v-show="step1"></step>
				<step v-show="step2"></step>
				<step v-show="step3"></step>
			</v-container>
		</v-content>
	</v-app>
</template>

<script>
	import step from "./components/step.vue"
	export default {
		components: {
			step
		}
	}
</script>
