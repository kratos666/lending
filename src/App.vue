<template>
	<v-app>
		<v-content>
			<v-container fluid>
				<step v-if="curStep1">step1</step>
				<step v-if="curStep2">step2</step>
				<step v-if="curStep3">step3</step>
			</v-container>
		</v-content>
	</v-app>
</template>

<script>
	import step from "./components/step.vue"
	export default {
		components: {
			step
		},
		data() {
			return {
				step: curStep1
			}
		},
	}
</script>
