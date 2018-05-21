<template name="button1">
	<v-card >
		<v-card-actions>
			<v-btn color="success" @click="nextStep"> >>> </v-btn>
			<v-btn color="danger" @click="prevStep"> //// </v-btn>
		</v-card-actions>
	</v-card>
</template>

<script>
	export default {
		data() {
			return {
			}
		},
		methods: {
			nextStep: function () {
				this.$emit('changeStep', 'step3')
			},
			prevStep: function () {
				this.$emit('changeStep', 'step1')
			}
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


