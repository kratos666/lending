<template name="step2">
	<v-container fluid fill-height justify-center class="bgMain st2">
		<transition   name="custom-classes-transition"
enter-active-class="animated tada"
leave-active-class="animated bounceOutRight">
			<v-card >
				<transition>
					<button1 step="2"></button1>
				</transition>
			</v-card>
		</transition>
	</v-container>
</template>

<script>
	import button1 from "./buttons/button1.vue"
	export default {
		data() {
			return {}
		}
	}
</script>

<style scoped>
.bgMain.st2{
	background-image: url("https://u01.appmifile.com/images/2017/04/15/3b766ec1-aea8-4f31-8b71-4eaec714fe42.jpg");
	background-size: cover;
}
.st2 .card{
	background-image: url("https://u01.appmifile.com/images/2017/04/15/7aaad7ae-81b2-4066-8f89-7abc9b8ffb2e.jpg");
	background-size: cover;
}
</style>


